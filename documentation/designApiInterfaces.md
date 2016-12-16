   В виду специфики архитектуры языков программирования obj-c и Swift большое количество логики приложения 
 реализуется в методах , связанных с циклом жизни приложения или во встроенных методах соответствующих  
 встроенных вьюконтроллерах.
 
 Интерфейс ленты:
 Компонент feedVC.swift:
 commentBtn_click(sender: AnyObject) Взаимодействует с commentVC;
 moreBtn_click(sender: AnyObject);
 func alert (title: String, message : String);
 func refresh();
 // reloading func with posts  after received notification
 func uploaded(notification:NSNotification);
 func loadPosts() Взаимодействует с postVC ;

 Компонент postVC.swift:
 func usernameBtn_click(sender: AnyObject) Взаимодействует с usersVC;
 func commentBtn_click(sender: AnyObject) Взаимодействует с commentVC;
 func moreBtn_click(sender: AnyObject)
 func alert (title: String, message : String);

 Модуль авторизации:
 Компонент signInVC.swift:
 func signInBtn_click(sender: AnyObject) взаимодействует с TabBarVC;
 func signUpBtn_click(sender: AnyObject) взаимодействует с SignUpVC через segue;
 logInWithUsernameInBackground(usernameTxt.text!, password: passwordTxt.text!);

 Компонент signUpVC.swift:
 func loadImg(recognizer:UITapGestureRecognizer);
 func imagePickerController(picker: UIImagePickerController, didFinishPickingMediaWithInfo info: [String : AnyObject]);
 func signUpBtn_click(sender: AnyObject) Взаимодействует с TabBarVC;
 func cancelBtn_click(sender: AnyObject)  Взаимодействует с signInVC;

 Компонент resetPassword.swift:
 func resetBtn_click(sender: AnyObject, email:String);
 func cancelBtn_click(sender: AnyObject) Взаимодействует с signInVC;
 
 Модуль навигации:
 Компонент tapbarVC.swift:
 func placeIcon (image:UIImage, text:String);
 func upload(sender : UIButton) ;
 func query (type:[String], image:UIImage);
  
 Компонент hashtagsVC.swift:
 func loadHashtags(hashtag:string) ищет посты по заданному хэштэгу;
 Модуль комментов:

 Компонент commentVC.swift:
 func loadComments() 
 func sendBtn_click(sender: AnyObject)
 func usernameBtn_click(sender: AnyObject) Взаимодействует с usersVC;
 func alert (title: String, message : String)

 Модуль пользователя:
 Компонент followersVC.swift:
 func loadFollowings();
 func loadFollowers();

 Компонент headerView.swift:
 followBtn_clicked(sender: AnyObject) реализовывается логика follow/unfollow. 
  Компонент userVC.swift:
  func loadUsers()
  func loadPosts()
  func loadMore() отобразить еще посты, если их больше, чем влазит во вью.
 Отдельные компоненты:

 Компонент uploadVC.swift:
 func selectImg() загрузка изображений, используя контроллер UIImagePickerView

 Компонент settings.swift:
 func validateEmail (email : String) -> Bool
 func validateWeb (web : String) -> Bool
 func information() запрашивает с сервера и выводит всю информацию о профиле пользователя.
 func save_clicked(sender: AnyObject)
 func cancel_clicked(sender: AnyObject) Взаимодействует с userVC;

 Компонент searchUser.swift:
 func searchBar(searchBar: UISearchBar, shouldChangeTextInRange range: NSRange, replacementText text: String) -> Bool
 func searchBarTextDidBeginEditing(searchBar: UISearchBar)

 Компонент Notifications:
 func usernameBtn_click(sender: AnyObject)
 func post_click(sender: AnyObject)

 
