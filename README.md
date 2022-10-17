# alertMenuTextInput


```swift

      func addNewProduct() {
        
        let menu = UIAlertController(title: "New Product", message: "", preferredStyle: .alert)
        
        menu.addTextField { nameTextField in
            nameTextField.placeholder = "name"
        }
        
        menu.addTextField { nameTextField in
            nameTextField.placeholder = "price"
        }
        
        let saveButton = UIAlertAction(title: "Save", style: .default) { data in
            let firstTextField = menu.textFields![0] as UITextField
            let secondTextField = menu.textFields![1] as UITextField
            
            print(firstTextField.text ?? "")
            print(secondTextField.text ?? "")
       
        }
       
        let cancelButton = UIAlertAction(title: "Cancel", style: .cancel)
       
        menu.addAction(saveButton)
        menu.addAction(cancelButton)
        present(menu, animated: true)
    }
