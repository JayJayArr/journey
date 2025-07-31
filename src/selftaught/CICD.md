# CI/CD & Testing

### Testing in general

After my first decently sized project I realized how much hassle I could have saved by using TDD in general.
By just writing tests for the software you are creating you gain an enourmous amount of trust in it.
At the same time the development cycle speeds up a lot. You suddenly can define when you are done and you can prove it.
Your tests pass and they check everything important - congrats, you are done!
Your tests don't pass or a feature is still not fully covered - back to the IDE champ...
For small projects I still prefer to omit tests, if you will never touch that piece of code again and you know it works why write the tests for it?
That of course only works if you REALLY never touch it again (no dependency update, no additional feature, you never compile it again, you never deploy it again, it is a prototype).

### CI/CD

CI/CD is the advanced stage of testing, you automate it.
Of course you should still run tests locally before you push, CI/CD does not replace a good testing or deployment process but it rather completes it.
The first time properly using CI/CD was when I went through Luca Palmieri's "Zero to Production in Rust" using axum instead of actix-web.
Testing in of itself was not a new concept, what was new to me was using integration tests to that extent.
You cannot make sure that the unit tests by themselves combine to do what the app is designed to do until you test the app as a whole.
And he created some excellent examples of how to do it properly!
Having a database spin up just for some tests is not a huge effort, I just never thought about it.
Having multiple databases on a postgres instance so that every test is isolated is genius (though I am curious until when it scales well).

At the moment I am not yet at a stage where I push straight to a branch just to run tests while I am still coding on a feature or debugging, but in the long run this could make sense depending on the CI setup.
If you are already doing that please share your experience with me!

### Setting up CI/CD

One tool I have become increasingly fond of is Act.
Act is a small command line extenstion to the gh cli which uses Docker to run the Actions you defined.
This saves you from pushing towards github multiple times just to debug your configured action runs possibly wasting CI minutes.
