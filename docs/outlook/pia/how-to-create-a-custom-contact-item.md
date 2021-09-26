---
title: Création d’un contact personnalisé
TOCTitle: Create a custom Contact item
ms:assetid: 24b2a104-a0a7-469b-9676-a07cab613f59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184596(v=office.15)
ms:contentKeyID: 55119831
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a885afdf724926029be84080704b3d6bfc21479a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623788"
---
# <a name="create-a-custom-contact-item"></a>Création d’un contact personnalisé

Cet exemple montre comment créer un élément de contact personnalisé et définir les propriétés prédéfinies et définies par l’utilisateur.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Un objet [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) représente un contact dans le dossier Contacts et comporte plus de 100 propriétés intégrées, dont [FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)) et [LastName](https://msdn.microsoft.com/library/bb609750\(v=office.15\)). Parfois, les propriétés intégrées ne sont pas suffisantes. Il faut alors ajouter des propriétés personnalisées, en utilisant la collection [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)).

Dans l’exemple de code suivant, CreateCustomItem crée un objet **ContactItem** personnalisé, le nomme « Shoe Store », et appelle la méthode [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) pour l’ajouter à un dossier nommé « Shoe Store ». CreateCustomItem obtient d’abord le dossier « Shoe Store » en utilisant la méthode [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)). Le dossier « Shoe Store » est un sous-dossier du dossier Contacts par défaut. CreateCustomItem définit ensuite les propriétés **FirstName** et **LastName**, puis crée une propriété définie par l’utilisateur (« Shoe Size ») en utilisant la collection **UserProperties**.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateCustomItem()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Folders[
        "Shoe Store"] as Outlook.Folder;
    Outlook.ContactItem contact =
        folder.Items.Add(
        "IPM.Contact.Shoe Store") as Outlook.ContactItem;
    contact.FirstName = "Michael";
    contact.LastName = "Affronti";
    contact.UserProperties["Shoe Size"].Value = "9";
    contact.Save();
}
```

## <a name="see-also"></a>Voir aussi

- [Contacts](contacts.md)

