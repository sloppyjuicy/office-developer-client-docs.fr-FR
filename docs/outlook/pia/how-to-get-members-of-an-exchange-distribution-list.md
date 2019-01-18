---
title: Obtenir les membres d’une liste de distribution Exchange
TOCTitle: Get members of an Exchange distribution list
ms:assetid: 75b38e40-772c-400b-8df9-e3e385b87f9c
ms:mtpsurl: https://msdn.microsoft.com/library/Bb645998(v=office.15)
ms:contentKeyID: 55119837
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: d5c615eb811d5dc4a0f4170bfe432179acaa4666
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726056"
---
# <a name="get-members-of-an-exchange-distribution-list"></a>Obtenir les membres d’une liste de distribution Exchange

Cet exemple invite l'utilisateur à sélectionner une liste de distribution Exchange dans la boîte de dialogue **Sélectionner des noms** et développe la liste de distribution de manière à afficher ses membres.

## <a name="example"></a>Exemple

Cet exemple de code appelle la méthode [GetExchangeDistributionListMembers](https://msdn.microsoft.com/library/bb647622\(v=office.15\)) de l'objet [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) pour obtenir une collection [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) contenant tous les membres de la liste. Dans la mesure où une liste de distribution peut être imbriquée dans une autre liste de distribution, la collection **AddressEntries** retournée peut représenter tout type d'objet [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) Exchange.


> [!NOTE]
> Le développement de listes de distribution peut réduire les performances sur un serveur Exchange. Par conséquent, utilisez la méthode **GetExchangeDistributionListMembers** avec parcimonie et attendez-vous à ce que votre code soit lent lorsqu'il développe de longues listes de distribution.

Pour obtenir les membres d’une liste de distribution, l’utilisateur doit être connecté à un serveur Exchange en ligne.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub GetDistributionListMembers()
    Dim snd As Outlook.SelectNamesDialog = _
        Application.Session.GetSelectNamesDialog()
    Dim addrLists As Outlook.AddressLists = _
        Application.Session.AddressLists
    For Each addrList As Outlook.AddressList In addrLists
        If addrList.Name = "All Groups" Then
            snd.InitialAddressList = addrList
            Exit For
        End If
    Next
    snd.NumberOfRecipientSelectors = _
        Outlook.OlRecipientSelectors.olShowTo
    snd.ToLabel = "D/L"
    snd.ShowOnlyInitialAddressList = True
    snd.AllowMultipleSelection = False
    snd.Display()
    If (snd.Recipients.Count > 0) Then
        Dim addrEntry As Outlook.AddressEntry = _
            snd.Recipients(1).AddressEntry
        If (addrEntry.AddressEntryUserType = _
            Outlook.OlAddressEntryUserType. _
            olExchangeDistributionListAddressEntry) Then
            Dim exchDL As Outlook.ExchangeDistributionList = _
                addrEntry.GetExchangeDistributionList()
            Dim addrEntries As Outlook.AddressEntries = _
                exchDL.GetExchangeDistributionListMembers()
            If Not (addrEntries Is Nothing) Then
                For Each exchDLMember As _
                    Outlook.AddressEntry In addrEntries
                    Debug.WriteLine(exchDLMember.Name)
                Next
            End If
         End If
    End If
End Sub
```


```csharp
private void GetDistributionListMembers()
{
    Outlook.SelectNamesDialog snd =
        Application.Session.GetSelectNamesDialog();
    Outlook.AddressLists addrLists =
        Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        if (addrList.Name == "All Groups")
        {
            snd.InitialAddressList = addrList;
            break;
        }
    }
    snd.NumberOfRecipientSelectors =
        Outlook.OlRecipientSelectors.olShowTo;
    snd.ToLabel = "D/L";
    snd.ShowOnlyInitialAddressList = true;
    snd.AllowMultipleSelection = false;
    snd.Display();
    if (snd.Recipients.Count > 0)
    {
        Outlook.AddressEntry addrEntry =
            snd.Recipients[1].AddressEntry;
        if (addrEntry.AddressEntryUserType ==
            Outlook.OlAddressEntryUserType.
            olExchangeDistributionListAddressEntry)
        {
            Outlook.ExchangeDistributionList exchDL =
                addrEntry.GetExchangeDistributionList();
            Outlook.AddressEntries addrEntries =
                exchDL.GetExchangeDistributionListMembers();
            if (addrEntries != null)
                foreach (Outlook.AddressEntry exchDLMember
                    in addrEntries)
                {
                    Debug.WriteLine(exchDLMember.Name);
                }
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Utilisateurs Exchange](exchange-users.md)

