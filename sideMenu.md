  Code in AppDelegate
  
  func setUpSideMenu()
    {
        let mainStoryboard : UIStoryboard = UIStoryboard(name: "Main", bundle: nil)
        
        let home: TabBarVC = mainStoryboard.instantiateViewController(withIdentifier: "TabBarVC") as! TabBarVC
        
        let homeNavigation = UINavigationController(rootViewController: home)
        
        let sideMenuVC = mainStoryboard.instantiateViewController(withIdentifier: "SideMenuVC") as! SideMenuVC
        
        let controller = LGSideMenuController.init(rootViewController: homeNavigation, leftViewController: sideMenuVC, rightViewController: nil)
        
        controller.leftViewWidth = 280
        
        self.window?.rootViewController = controller
        self.window?.makeKeyAndVisible()
    }
    
    //MARK: - Code in viewcontroller
    
    self.sideMenuController?.showLeftView(animated: true, completion: nil)
