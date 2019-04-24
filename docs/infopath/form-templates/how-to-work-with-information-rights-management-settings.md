---
title: Utiliser les paramètres de gestion des droits relatifs à l'information
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- information rights management [infopath 2007],InfoPath 2007, Information Rights Management,IRM [InfoPath 2007]
localization_priority: Normal
ms.assetid: 4ad91898-b23e-4410-8839-a65259e53d37
description: "Il existe deux types de paramètres de Gestion des droits relatifs à l'information (IRM) dans Microsoft InfoPath : l'un protège l'accès aux modèles de formulaires InfoPath et l'autre permet de contrôler l'accès aux données contenues dans les formulaires complétés et les actions sur ces données."
ms.openlocfilehash: 6f7317cfdc4e6bfc89482e813b1670c8b8861a6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299789"
---
# <a name="work-with-information-rights-management-settings"></a>Utiliser les paramètres de gestion des droits relatifs à l'information

Il existe deux types de paramètres de Gestion des droits relatifs à l'information (IRM) dans Microsoft InfoPath : l'un protège l'accès aux modèles de formulaires InfoPath et l'autre permet de contrôler l'accès aux données contenues dans les formulaires complétés et les actions sur ces données.
  
> [!NOTE]
> [!REMARQUE] La restriction des autorisations est uniquement disponible pour les modèles de formulaires compatibles avec l'éditeur d'InfoPath. Les modèles de formulaires compatibles avec le navigateur ne prennent pas en charge la gestion des droits relatifs à l'information. 
  
## <a name="adding-the-manage-credentials-command-to-the-quick-access-toolbar"></a>Ajout de la commande Gérer les informations d’identification à la barre d’outils Accès rapide

La commande **Gérer les informations d’identification** utilisée pour travailler avec des paramètres de gestion des droits relatifs à l’information lors de la conception d’un modèle de formulaire n’est pas disponible par défaut. Procédez selon les étapes suivantes pour l’ajouter à la **Barre d’outils Accès rapide**.
  
### <a name="add-the-manage-credentials-command-to-the-quick-access-toolbar"></a>Ajouter la commande Gérer les informations d’identification à la barre d’outils Accès rapide

1.  Cliquez sur la flèche située à l'extrémité droite de la **Barre d'outils Accès rapide** pour dérouler le menu **Personnaliser la barre d'outils Accès rapide**, puis cliquez sur **Autres commandes**.
    
2. Dans la liste **Choisir les commandes dans les catégories suivantes**, sélectionnez **Toutes les commandes**.
    
3. Faites défiler la liste jusqu'à **Gérer les informations d'identification**, puis cliquez sur **Ajouter**.
    
4. Cliquez sur **OK**.
    
Pour plus d’informations sur l’utilisation de la commande **Gérer les informations d’identification** et de la boîte de dialogue **Autorisation** dans InfoPath, voir la rubrique « Créer un modèle de formulaire avec des autorisations restreintes » dans l’aide d’InfoPath. 
  
## <a name="the-irm-object-model"></a>Modèle objet Gestion des droits relatifs à l'information (IRM)

Utilisez la classe [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) pour accéder aux paramètres d'autorisation [UserPermissionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.aspx) et aux paramètres d'autorisation de la Gestion des droits relatifs à l'information, applicables à un formulaire. Pour accéder à l'objet **Permission** associé à un modèle de formulaire, utilisez la propriété [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . L'objet **Permission** retourné fournit l'accès à la collection d'objets [UserPermission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.aspx) associés au modèle de formulaire et à chaque instance du formulaire créée à l'aide de ce modèle. 
  
L'objet **Permission**, ses propriétés et ses méthodes sont accessibles indépendamment des restrictions d'autorisations appliquées au modèle de formulaire actif. Utilisez la propriété [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) pour déterminer si un formulaire contient des autorisations restreintes. 
  
Les autorisations d'un formulaire sont activées de l'une des manières suivantes à l'aide des propriétés et méthodes de la classe Permission :
  
La propriété **Enabled** est définie sur la valeur **true**.
  
La propriété [DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) est définie. 
  
La propriété [RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) est définie. 
  
La propriété [StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) est définie sur la valeur **true** ou **false**.
  
La méthode [ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) est appelée. 
  
> [!NOTE]
> [!REMARQUE] Si le client Windows Rights Management n'est pas installé sur l'ordinateur d'un utilisateur, l'utilisation de la classe **Permission** génère une exception. 
  
Pour utiliser par programmation les paramètres de la Gestion des droits relatifs à l'information au niveau des utilisateurs individuels dans les formulaires, utilisez les classes **UserPermissionCollection** et **UserPermission**. 
  
Un objet **UserPermission** associe un jeu d'autorisations du formulaire actuel à un seul utilisateur et à une date d'expiration facultative. Utilisez la méthode [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) de la classe **UserPermissionCollection** pour ajouter ou attribuer un jeu d'autorisations à un utilisateur sur le formulaire actuel. Utilisez la méthode [Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx) de la classe **UserPermissionCollection** pour supprimer un utilisateur et les autorisations associées. Tandis que certaines autorisations sont accordées à l'ensemble des utilisateurs par l'intermédiaire de l'interface utilisateur, notamment l'autorisation d'impression et la date d'expiration, vous pouvez également attribuer des autorisations à chaque utilisateur individuellement et définir des dates d'expiration spécifiques à chacun d'eux à l'aide des classes **UserPermission** et **UserPermissionCollection**. Le modèle objet permet aux développeurs d'énumérer les paramètres d'autorisation dans un formulaire et de fournir les fonctionnalités qui permettent aux utilisateurs de formulaires d'ajouter des autorisations au formulaire sans devoir utiliser le volet Office **Autorisation du formulaire** ou la boîte de dialogue **Autorisation**. 
  
> [!NOTE]
> [!REMARQUE] Aucune autorisation ne peut être appliquée lorsqu'un formulaire est affiché en mode Aperçu. Ainsi, toutes les propriétés de la classe **Permission** sont en lecture seule dans l'aperçu du formulaire. En mode Aperçu, la propriété **Enabled** retourne toujours la valeur **false** et, si le code essaie de modifier ce paramètre, une exception **System.Runtime.InteropServices.COMException** est générée et l'erreur « La propriété/méthode n'est pas disponible en mode Aperçu » est retournée. De même, les méthodes associées aux classes **UserPermission** et **UserPermissionCollection** retournent également ce message d'erreur lorsqu'elles sont utilisées en mode Aperçu. 
  
### <a name="overview-of-the-permission-class"></a>Vue d'ensemble de la classe des  autorisations

La classe **UserPermissionCollection** fournit les propriétés suivantes et une méthode. 
  
|**Nom**|**Description**|
|:-----|:-----|
|[ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) , méthode  <br/> |Applique une stratégie au formulaire en utilisant un fichier de modèle de stratégie.  <br/> |
|[DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) , propriété  <br/> |Obtient ou définit l'auteur du formulaire actuel sous la forme d'une adresse de messagerie.  <br/> |
|[Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) , propriété  <br/> |Obtient ou définit l'information indiquant que les paramètres d'autorisation représentés par l'objet **Permission** sont activés pour le formulaire actif.  <br/> |
|[PermissionFromPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PermissionFromPolicy.aspx) , propriété  <br/> |Obtient ou définit l'application d'une stratégie d'autorisation pour le formulaire actif.  <br/> |
|[PolicyDescription](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyDescription.aspx) , propriété  <br/> |Obtient une description de la stratégie appliquée au formulaire actif.  <br/> |
|[PolicyName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyName.aspx) , propriété  <br/> |Obtient le nom de la stratégie appliquée au formulaire actif.  <br/> |
|[RequestPermissionURL](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) , propriété  <br/> |Obtient ou définit le fichier, l'URL ou l'adresse de messagerie à contacter pour les utilisateurs qui ont besoin d'autorisations supplémentaires sur le formulaire actif.  <br/> |
|[StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) , propriété  <br/> |Obtient ou définit l'information indiquant que la licence permettant à l'utilisateur d'afficher le formulaire actif doit être mise en cache pour permettre son affichage en mode hors connexion lorsque l'utilisateur ne peut pas se connecter à un serveur de gestion des droits.  <br/> |
|[Autorisationsdes utilisateurs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.UserPermissions.aspx) , propriété  <br/> |Obtient un objet **UserPermissionCollection** pour le formulaire actuel.  <br/> |
   
### <a name="overview-of-the-userpermissioncollection-class"></a>Vue d'ensemble de la classe UserPermissionCollection

La classe **UserPermissionCollection** fournit les propriétés et les méthodes suivantes. 
  
|**Nom**|**Description**|
|:-----|:-----|
|[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) , méthode (+ 3 Overloads)  <br/> |Ajoute un nouvel utilisateur au formulaire actuel, en spécifiant éventuellement des autorisations et une date d'expiration.  <br/> |
|Méthode [Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx)  <br/> |Supprime l'objet **UserPermission** comportant l'ID **UserId** spécifié à partir de la collection.  <br/> |
|[RemoveAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.RemoveAll.aspx) , méthode  <br/> |Supprime tous les objets **UserPermission** de la collection.  <br/> |
|Propriété [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Count.aspx)  <br/> |Obtient le nombre d'objets **UserPermission** dans la collection.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) , propriété (+ 1 Overload)  <br/> |Obtient un objet **UserPermission**.  <br/> |
   
### <a name="overview-of-the-userpermission-class"></a>Vue d'ensemble de la classe UserPermission

La classe **UserPermission** fournit les propriétés suivantes et une méthode. 
  
|**Nom**|**Description**|
|:-----|:-----|
|Méthode [Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Remove.aspx)  <br/> |Supprime l'objet **UserPermission** actuel des autorisations du formulaire.  <br/> |
|[ExpirationDate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.ExpirationDate.aspx) , propriété  <br/> |Obtient ou définit la date d'expiration facultative pour les autorisations du formulaire actif affectées à l'utilisateur associé à une instance de la classe **UserPermission**.  <br/> |
|[Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Permission.aspx) , propriété  <br/> |Obtient ou définit une valeur représentant les autorisations du formulaire actif affectées à l'utilisateur associé à une instance de la classe **UserPermission**.  <br/> |
|[Userid](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.UserId.aspx) , propriété  <br/> |Obtient l'adresse de messagerie de l'utilisateur dont les autorisations sur le formulaire actif sont déterminées par l'objet **UserPermission** spécifié.  <br/> |
   
### <a name="the-permissiontype-enumeration"></a>Énumération PermissionType

Les autorisations d'un utilisateur sont définies ou lues à l'aide des valeurs d'énumération [PermissionType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.aspx) . 
  
|**Nom**|**Description**|
|:-----|:-----|
|**PermissionType. change** <br/> |Permet aux utilisateurs d'afficher, de copier et d'enregistrer un formulaire mais pas de l'imprimer. Elle correspond à la combinaison des autorisations **Read**, **Edit**, **Save** et **Extract**.  <br/> |
|**PermissionType. Edit** <br/> |Permet à l'utilisateur de modifier le formulaire.  <br/> |
|**PermissionType. Extract** <br/> |Permet à un utilisateur disposant de l'autorisation **Read** de copier un contenu dans le formulaire.  <br/> |
|**PermissionType. contrôle total** <br/> |Permet à l'utilisateur d'ajouter, de modifier et de supprimer les autorisations d'autres utilisateurs d'un formulaire.  <br/> |
|**PermissionType. ObjectModel** <br/> |Permet à un utilisateur d'accéder au document du formulaire par programme via son modèle objet. Les utilisateurs qui ne disposent pas de l'autorisation **ObjectModel** ne peuvent pas avoir recours au modèle objet pour déterminer leurs propres autorisations.  <br/> |
|**PermissionType. Print** <br/> |Permet à l'utilisateur d'imprimer le formulaire.  <br/> |
|**PermissionType. Read** <br/> |Permet à l'utilisateur de lire (d'afficher) le formulaire. (Les autorisations **Read** et **View** sont équivalentes.)  <br/> |
|**PermissionType. Save** <br/> |Permet à l'utilisateur d'enregistrer le formulaire.  <br/> |
|**PermissionType. View** <br/> |Permet à l'utilisateur d'afficher (de lire) le formulaire. (Les autorisations **Read** et **View** sont équivalentes.)  <br/> |
   
### <a name="example"></a>Exemple

Dans l'exemple ci-dessous, le contrôle **Bouton** permet d'obtenir la collection **UserPermissionsCollection** pour le formulaire actif, d'ajouter et d'attribuer un utilisateur au niveau d'accès Modification, ainsi que de définir une date d'expiration de deux jours à compter de la date du jour. 
  
```cs
public void CTRL1_Clicked(object sender, ClickedEventArgs e)
{
   string strExpirationDate = DateTime.Today.AddDays(2).ToString();
   DateTime dtExpirationDate = DateTime.Parse(strExpirationDate);
   this.Permission.UserPermissions.Add("someone@example.com", 
      PermissionType.Change, dtExpirationDate);
}
```

```vb
Public Sub CTRL1_Clicked(ByVal sender As Object, _
   ByVal e As ClickedEventArgs)
   Dim strExpirationDate As String = _
      DateTime.Today.AddDays(2).ToString()
   dtExpirationDate As DateTime = DateTime.Parse(strExpirationDate)
   Me.Permission.UserPermissions.Add("someone@example.com", _
      PermissionType.Change, dtExpirationDate)
End Sub
```


