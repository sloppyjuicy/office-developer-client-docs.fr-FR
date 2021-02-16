---
title: 'Procédure pas à pas : créer un modèle de formulaire de base avec du code'
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- form templates [infopath 2007], creating managed code,managed code form templates [InfoPath 2007], creating,form templates [InfoPath 2007], walkthroughs,InfoPath 2007, walkthroughs
localization_priority: Normal
ms.assetid: 0f55c8be-8641-476a-b0c8-c88adb2ac2b9
description: Dans Microsoft InfoPath, vous pouvez écrire une logique métier en Visual Basic ou C# en ouvrant un modèle de formulaire dans le concepteur InfoPath, puis en utilisant l’une des commandes d’interface utilisateur pour ajouter un handler d’événements, qui ouvre l’environnement de développement Visual Studio 2012 pour écrire votre code.
ms.openlocfilehash: cc09856750ced28d35c8da172a08a31c4e3cd4a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420646"
---
# <a name="walkthrough-create-a-basic-form-template-with-code"></a>Procédure pas à pas : créer un modèle de formulaire de base avec du code

Dans Microsoft InfoPath, vous pouvez écrire une logique métier en Visual Basic ou C# en ouvrant un modèle de formulaire dans le concepteur InfoPath, puis en utilisant l’une des commandes d’interface utilisateur pour ajouter un handler d’événements, qui ouvre l’environnement de développement Visual Studio 2012 pour écrire votre code. Par défaut, les projets de modèle de formulaire créés Visual Studio 2012 fonctionnent sur le modèle objet avec code géré fourni par l’espace de noms [Microsoft.Office.InfoPath.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 
  
Cette procédure pas à pas vous montre tout d’abord comment créer une application Hello World simple en C# ou Visual Basic dans l’environnement de développement Visual Studio 2012. La procédure pas à pas se termine par un exemple de code qui vous montre comment utiliser la propriété [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) de la classe [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) pour récupérer le nom de l’utilisateur actuel et remplir un contrôle **zone** de texte avec cette valeur. 
  
## <a name="prerequisites"></a>Configuration requise

Pour effectuer cette walkthrough à l’aide de l Visual Studio de développement 2012, vous aurez besoin des ressources ci-après :
  
- Microsoft InfoPath avec Visual Studio 2012 installé.
    
## <a name="hello-world-in-visual-studio-tools-for-applications"></a>Créer l'application « Hello World » dans Visual Studio Tools for Applications

Dans la procédure pas à pas suivante, vous allez apprendre à écrire du code dans l’environnement de développement Visual Studio 2012 pour afficher une boîte de dialogue d’alerte simple en écrivant un handler d’événements pour l’événement [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) de la classe [ButtonEvent,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) qui est associée au contrôle **Button.** 
  
### <a name="create-a-new-project-and-specify-the-programming-language"></a>Créer un projet et spécifier le langage de programmation

1. Démarrez le Concepteur InfoPath, puis double-cliquez sur le modèle de formulaire **Vide  (Éditeur InfoPath)**. 
    
2. Pour spécifier le langage de programmation à utiliser, cliquez sur le **bouton Microsoft Office**, cliquez sur **Options de formulaire**, cliquez sur **Programmation** dans la liste **Catégorie**, puis sélectionnez **Visual Basic** ou **C#** dans la liste déroulante **Langage de code du modèle de formulaire**. 
    
   > [!NOTE]
   > Les autres options de langage de programmation dans la liste déroulante **Langage de code du modèle de formulaire** indiquent la compatibilité avec les versions précédentes d'InfoPath. Les options **C# (compatibles InfoPath 2007)** et **Visual Basic (compatible InfoPath 2007)** fonctionnent avec les procédures mentionnées dans cette rubrique. Cependant, pour utiliser les options **C# (compatible InfoPath 2003)** et **Visual Basic (compatible InfoPath 2003)**, voir [Procédure pas à pas : Création et débogage d'un modèle de formulaire de base avec le modèle objet InfoPath 2003](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md). 
  
    Vous pouvez à présent ajouter un contrôle **Bouton** et créer son gestionnaire d'événements. 
    
### <a name="add-a-button-control-and-event-handler"></a>Ajouter un contrôle Bouton et un gestionnaire d'événements

1. Dans le groupe **Contrôles**, cliquez sur le contrôle **Bouton** pour l'ajouter au formulaire. 
    
2. Double-cliquez sur le contrôle **Bouton**, tapez Hello pour la propriété **Étiquette** sous l'onglet **Propriétés** du ruban, puis cliquez sur **Code personnalisé**. Lorsque vous y êtes invité, enregistrez le formulaire et nommez-le HelloWorld.
    
   Cela ouvre **l’environnement Visual Studio Tools for Applications** avec le curseur dans le handler d’événements pour l’événement [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) du **contrôle Button.** 
    
   Vous pouvez maintenant ajouter du code de formulaire au gestionnaire d'événements du bouton. 
    
### <a name="add-hello-world-code-to-the-event-handler-and-preview-the-form"></a>Ajouter le code « Hello World » au gestionnaire d'événements et afficher un aperçu du formulaire

1. Dans le squelette du gestionnaire d'événements, tapez :
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   Le code de votre modèle de formulaire doit se présenter ainsi :
    
   ```cs
    using Microsoft.Office.InfoPath;
    using System;
    using System.Windows.Forms;
    using System.Xml;
    using System.Xml.XPath;
    namespace HelloWorld
    {
        public partial class FormCode
        {
            public void InternalStartup()
            {
            ((ButtonEvent)EventManager.ControlEvents["CTRL1_5"]).Clicked += new ClickedEventHandler(CTRL1_5_Clicked);
            }
            public void CTRL1_5_Clicked(object sender, ClickedEventArgs e)
            {
            MessageBox.Show("Hello World!");
            }
        }
    }
   ```

   ```vb
    Imports Microsoft.Office.InfoPath
    Imports System
    Imports System.Windows.Forms
    Imports System.Xml
    Imports System.Xml.XPath
    Namespace HelloWorld
        Public Class FormCode
            Private Sub InternalStartup(ByVal sender As Object, ByVal e As EventArgs) Handles Me.Startup
            AddHandler DirectCast(EventManager.ControlEvents("CTRL1_5"), ButtonEvent).Clicked, AddressOf CTRL1_5_Clicked
            End Sub
            Public Sub CTRL1_5_Clicked(ByVal sender As Object, ByVal e As ClickedEventArgs)
            MessageBox.Show("Hello World!")
            End Sub
        End Class
    End Namespace
   ```

2. Basculez dans la fenêtre Concepteur InfoPath.
    
3. Cliquez sur le bouton **Aperçu** sous l'onglet **Accueil**. 
    
4. Cliquez sur le bouton Hello du formulaire. 
    
   Un message s'affiche avec le texte « Hello World! ».
    
   La procédure suivante illustre l'ajout de points d'arrêt pour le débogage dans le code de votre formulaire.
    
### <a name="debug-form-code"></a>Débogage de code de formulaire

1. Revenir à la fenêtre Visual Studio 2012.
    
2. Cliquez sur la barre grise située à gauche de la ligne :
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   Un cercle rouge s'affiche et la ligne de code est mise en surbrillance pour indiquer que l'exécution marquera une pause à ce point d'arrêt dans votre code de formulaire.
    
3. Dans le menu **Débogage**, cliquez sur **Démarrer le débogage** ou appuyez sur F5. 
    
4. Dans la fenêtre **Aperçu** d'InfoPath, cliquez sur le bouton Hello du formulaire.  
    
5. L Visual Studio éditeur de code 2012 est mis au point et la ligne de point d’arrêt est mise en surbrillant.
    
6. Dans le menu **Débogage**, cliquez sur **Pas à pas principal** (ou appuyez sur Maj+F8 pour continuer pas à pas dans le code). 
    
7. Le gestionnaire d'événements est exécuté, et le message « Hello World! » s'affiche.  
    
8. Cliquez **sur OK** pour revenir à l’éditeur de code  Visual Studio 2012, puis cliquez sur Arrêter le débogage dans le menu **Débogage** (ou appuyez sur Ctrl+Alt+Arrêt). 
    
## <a name="getting-the-current-users-name"></a>Obtention du nom de l’utilisateur actuel

Dans l’exemple suivant, vous allez apprendre à utiliser la propriété [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) de la classe [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx)  pour récupérer le nom de l’utilisateur actuel et remplir la valeur d’un contrôle zone de texte à l’aide d’un handler d’événements pour l’événement [Loading.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) 
  
Pour remplir le contrôle **Zone** de texte, vous pouvez utiliser une instance de la classe [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) pour écrire le nom de l’utilisateur actuel dans le nœud XML lié au contrôle. 
  
Tout d’abord, la propriété [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) est appelée pour récupérer une instance de la classe [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) qui représente le document XML sous-jacent du formulaire. L’objet [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) appelle ensuite la méthode [CreateNavigator,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) qui crée l’objet **XPathNavigator** et le positionne au niveau du nœud racine de la source de données principale du formulaire. 
  
La [méthode SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) de la classe **XPathNavigator** est appelée pour sélectionner le champ employé dans la source de données du formulaire. Enfin, la [méthode SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) est appelée pour définir la valeur du champ avec la [propriété UserName.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) 
  
Pour plus d’informations sur **l'System.Xml** dans les modèles de formulaires avec code manadé, voir Utiliser les [classes XPathNavigator et XPathNodeIterator.](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md)
  
### <a name="add-a-loading-event-handler"></a>Ajouter un gestionnaire d'événements Chargement en cours (Loading)

1. Ouvrez le modèle de formulaire HelloWorld que vous avez créé dans la procédure pas à pas précédente dans le Concepteur InfoPath.
    
2. Sous l'onglet **Affichage**, sélectionnez **Afficher les champs**.
    
3. Cliquez avec le bouton droit sur le dossier **mesChamps**, puis cliquez sur **Ajouter**.
    
4. Dans **Nom,** tapez employé, puis cliquez sur **OK**.
    
5. Faites glisser le champ Employé dans la vue. 
    
6. Sous l'onglet **Développeur**, cliquez sur **Événement Chargement en cours (Loading)**.
    
   Cela crée un handler d’événements pour l’événement [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) et déplace la mise au point sur ce dernier dans l’éditeur de code. 
    
7. Dans l'éditeur de code, tapez le code suivant :
    
   ```cs
    public void FormEvents_Loading(object sender, LoadingEventArgs e)
    {
        XPathNavigator dataSource;
        dataSource = this.MainDataSource.CreateNavigator();
        dataSource.SelectSingleNode(
            "/my:myFields/my:employee", NamespaceManager).SetValue(this.User.UserName);
    }
   ```
 
   ```vb
    Public Sub FormEvents_Loading(ByVal sender As Object, ByVal e As LoadingEventArgs)
        Dim dataSource As XPathNavigator
        dataSource = Me.MainDataSource.CreateNavigator
        dataSource.SelectSingleNode( _
            "/my:myFields/my:employee", NamespaceManager).SetValue(Me.User.UserName)
    End Sub
   ```

8. Basculez dans la fenêtre de création de formulaire d'InfoPath, puis cliquez sur le bouton **Aperçu** de l'onglet **Accueil** pour afficher le formulaire. 
    
   Le champ employé doit être renseigné automatiquement avec votre nom d'utilisateur. 
    
## <a name="next-steps"></a>Étapes suivantes

- Pour plus d’informations sur l’working with event handlers for other controls and events, see [Add an Event Handler](how-to-add-an-event-handler.md).
    
- Pour plus d’informations sur l’aperçu et le débogage du code dans les modèles de formulaire, voir Aperçu et débogage des modèles de formulaire [InfoPath avec code.](how-to-preview-and-debug-infopath-form-templates-with-code.md)
    
- Pour plus d’informations sur le déploiement d’un modèle de formulaire avec code géré, voir Déployer des modèles de formulaire [InfoPath avec code.](how-to-deploy-infopath-form-templates-with-code.md)
    
- Pour plus d'informations sur le modèle objet InfoPath et les tâches de programmation courantes dans les modèles de formulaire avec code managé, voir [Modèle objet InfoPath et tâches de développement courantes](understanding-the-infopath-object-model-and-common-developer-tasks.md).
    
## <a name="see-also"></a>Voir aussi

- [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)

