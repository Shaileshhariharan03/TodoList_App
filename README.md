# Todo List App 📋

This is a simple Todo List app built using SwiftUI. The app allows users to create, update, and delete tasks. The tasks are displayed in a list format, and users can mark tasks as completed or pending with a simple tap.

## Features ✨

- **Add Tasks**: Easily add new tasks to your to-do list.
- **Mark as Completed**: Toggle the completion status of tasks with a tap.
- **Edit Tasks**: Rearrange tasks by dragging and dropping them.
- **Delete Tasks**: Swipe to delete tasks.
- **Simple UI**: Clean and minimalistic design using SwiftUI.


## Screenshots 📱
<img src="https://github.com/user-attachments/assets/33e73cbf-3d63-4c0b-89e0-bcbdaa714960" width=200>
<img src="https://github.com/user-attachments/assets/f615f71d-a81e-4edd-878f-43f9dc78e854" width=200>
<img src="https://github.com/user-attachments/assets/1ff649fe-3e71-4474-87fa-32787aa3bc11" width=200>

## Requirements 📋

- iOS 15.0+
- Xcode 13+
- Swift 5.5+

## Installation 🛠️

1. Clone the repository:
   git clone https://github.com/Shaileshhariharan03/TodoList_App.git
   
2. Open the project in Xcode:
   bash
   cd todolist-swiftui
   open TodoList.xcodeproj
   
3. Build and run the project on a simulator or a physical device.

## Project Structure 📂

- `ListView.swift`: The main view that displays the list of tasks.
- `AddView.swift`: The view for adding a new task.
- `ListRowView.swift`: The view for displaying a single task in the list.
- `ListViewModel.swift`: The view model responsible for managing the tasks.
- `ItemModel.swift`: The model representing a single task.

## How It Works 🛠️

- The `ListViewModel` class is responsible for managing the list of tasks. It uses an array of `ItemModel` objects to store the tasks.
- Each task is represented by an `ItemModel` that contains an `id`, `title`, and `isCompleted` status.
- The `ListView` displays the tasks using a `List` component, and each task is rendered using the `ListRowView`.
- The `AddView` allows users to input a new task, which is then added to the list when the "Save" button is pressed.

## Code Snippets 🧑‍💻

### Adding a New Task

func saveButtonPressed() {
    if textIsAppropriate() {
        listViewModel.addItem(title: textFieldText)
        presentationMode.wrappedValue.dismiss()
    }
}

### Marking a Task as Completed

func updateItem(item: ItemModel) {
    if let index = items.firstIndex(where: { $0.id == item.id }) {
        items[index] = item.updateCompletion()
    }
}

## Contributing 🤝

Contributions are welcome! If you find any bugs or want to add a new feature, feel free to open an issue or create a pull request.

## Contact 📧

Feel free to reach out if you have any questions or suggestions:

- Email: hariharanshailesh@gmail.com
- GitHub: [Shaileshhariharan03](https://github.com/Shaileshhariharan03)


### Key Sections:

- **Introduction**: A brief overview of the app and what it does.
- **Features**: List of functionalities in the app.
- **Screenshots**: Add links or images to show the app's UI.
- **Requirements**: Specifies the iOS and Xcode versions needed.
- **Installation**: Step-by-step guide on how to set up the project.
- **Project Structure**: Overview of the key files and their roles.
- **How It Works**: Explanation of how the main components interact.
- **Code Snippets**: Examples of key parts of the code.
- **Contributing**: Instructions on how others can contribute to the project.
