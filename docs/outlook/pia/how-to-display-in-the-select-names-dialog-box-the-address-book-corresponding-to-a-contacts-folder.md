---
title: Affichage du carnet d’adresses lié à un dossier Contacts dans la boîte de dialogue Sélectionner des noms
TOCTitle: Display in the Select Names dialog box the address book corresponding to a Contacts folder
ms:assetid: 6cbfc843-51b5-4841-bbb1-14b93a35ba78
ms:mtpsurl: https://msdn.microsoft.com/library/Bb610437(v=office.15)
ms:contentKeyID: 55119799
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 8aa7093b26366f5aa47ce054b27eff04d48889b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405790"
---
# <a name="display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder"></a>Affichage du carnet d’adresses lié à un dossier Contacts dans la boîte de dialogue Sélectionner des noms

Cet exemple montre comment obtenir le carnet d'adresses correspondant au dossier Contacts par défaut, puis comment l'afficher dans la boîte de dialogue **Sélectionner des noms**.

## <a name="example"></a>Exemple

Dans Outlook, tous les carnets d'adresses sont représentés sous forme de collection par la propriété [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) de l'objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) . Cet exemple de code utilise la méthode [GetContactsFolder](https://msdn.microsoft.com/library/bb609225\(v=office.15\)) de l'objet [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) pour trouver le dossier de contacts qui correspond à chaque liste d'adresses. Chaque dossier Outlook possède un ID d'entrée. Comparez l'ID d'entrée du dossier Contacts par défaut à l'ID d'entrée d'un dossier Contact pour produire l' AddressList correspondant au dossier Contacts par défaut.

Avant d'afficher la liste d'adresses correspondant au dossier Contacts par défaut dans la boîte de dialogue **Sélectionner des noms**, l'exemple de code la définit comme valeur de la propriété [InitialAddressList](https://msdn.microsoft.com/library/bb646633\(v=office.15\)) de l'objet [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) .

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ShowContactsFolderAsInitialAddressList()
    Dim addrLists As Outlook.AddressLists
    Dim contactsFolder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderContacts), _
        Outlook.Folder)
    addrLists = Application.Session.AddressLists
    For Each addrList As Outlook.AddressList In addrLists
        Dim testFolder As Outlook.Folder = _
        CType(addrList.GetContactsFolder(), Outlook.Folder)
        If Not (testFolder Is Nothing) Then
            ' Test to determine if Folder returned
            ' by GetContactsFolder has same EntryID
            ' as default Contacts folder.
            If (Application.Session.CompareEntryIDs( _
                contactsFolder.EntryID, testFolder.EntryID)) Then
                Dim snd As Outlook.SelectNamesDialog = _
                    Application.Session.GetSelectNamesDialog()
                snd.InitialAddressList = addrList
                snd.Display()
            End If
        End If
    Next
End Sub
```


```csharp
private void ShowContactsFolderAsInitialAddressList()
{
    Outlook.AddressLists addrLists;
    Outlook.Folder contactsFolder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts)
        as Outlook.Folder;
    addrLists = Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        Outlook.Folder testFolder =
            addrList.GetContactsFolder() as Outlook.Folder;
        if (testFolder != null)
        {
            // Test to determine if Folder returned
            // by GetContactsFolder has same EntryID
            // as default Contacts folder.
            if (Application.Session.CompareEntryIDs(
                contactsFolder.EntryID, testFolder.EntryID))
            {
                Outlook.SelectNamesDialog snd =
                    Application.
                    Session.GetSelectNamesDialog();
                snd.InitialAddressList = addrList;
                snd.Display();
             }
         }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Carnet d’adresses](address-book.md)

