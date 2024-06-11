## Usage

It's easy to use.
Just download the `LoadingViewController` file and drag & drop it into your project.

We can use it with new structured concurrency like:

```swift
Task {
    LoadingView.show()
    OR
    LoadingView.hide()
}

If you are using the MVVM-C architecture:

Task {
    do {
        LoadingView.show()
        try await viewModel.fetchDataAPI()
        LoadingView.hide()
    } catch let err {
        LoadingView.hide()
        debugPrint(err.localizedDescription)
    }
}


