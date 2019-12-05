---
title: Obtenir la Liste d’Adresses Globale ou d’un ensemble de listes d’adresses pour un magasin
TOCTitle: Get the Global Address List or a set of address lists for a store
ms:assetid: a361ac58-25c6-4ce1-97b0-403ad67ee7a4
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-get-the-global-address-list-or-a-set-of-address-lists-for-a-store
ms:contentKeyID: 55119800
ms.date: 12/03/2019
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7f0f7ba9b8854603646dc41e1017c2465c4af2d8
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819328"
---
# <a name="get-the-global-address-list-or-a-set-of-address-lists-for-a-store"></a>Obtenir la Liste d’Adresses Globale ou d’un ensemble de listes d’adresses pour un magasin

Cette rubrique contient deux exemples de code qui montrent comment obtenir la liste d'adresses globale associée à un magasin et comment obtenir toutes les listes d'adresses associées à un magasin.

## <a name="example"></a>Exemple

Dans une session Microsoft Outlook où plusieurs comptes Microsoft Exchange sont définis dans le profil, plusieurs listes d'adresses peuvent être associées à un magasin. Dans chacun des exemples de code suivants, le magasin spécifique qui nous intéresse est le magasin du dossier actif affiché dans l'explorateur actif, mais l'algorithme permettant d'obtenir une liste d'adresses globale ou un ensemble d'objets [AddressList](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist?redirectedfrom=MSDN&view=outlook-pia) pour un magasin s'applique à n'importe quel magasin Exchange.

Le premier exemple de code contient la méthode DisplayGlobalAddressListForStore ainsi que la fonction GetGlobalAddressList. La méthode DisplayGlobalAddressListForStore affiche, dans la boîte de dialogue**Sélectionner des Noms**, la Liste d'adresses Globale associée au magasin actuel. DisplayGlobalAddressListForStore obtient d’abord le magasin actif. S'il s'agit d'un magasin Exchange, la fonction GetGlobalAddressList est appelée pour obtenir la Liste d'Adresses Globale associée au magasin actif. 

GetGlobalAddressList utilise l'objet [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia) et la propriété MAPIhttps://schemas.microsoft.com/mapi/proptag/0x3D150102pour obtenir la propriété PR\_EMSMDB\_SECTION\_UID d'une liste d'adresses et du magasin actif. GetGlobalAddressList identifie une liste d'adresses comme étant associée à un magasin si leurs propriétés PR\_EMSMDB\_SECTION\_UID correspondent, et si la liste d'adresses est la Liste d'Adresses Globale si sa propriété [AddressListType](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist.addresslisttype?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_AddressList_AddressListType) a la valeur [olExchangeGlobalAddressList](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.oladdresslisttype?redirectedfrom=MSDN&view=outlook-pia). Si l’appel à GetGlobalAddressList réussit, DisplayGlobalAddressListForStore utilise l’objet [SelectNamesDialog]https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.selectnamesdialog?redirectedfrom=MSDN&view=outlook-pia\) (objet pour afficher la liste d’adresses globale renvoyée dans la boîte de dialogue **Sélectionner des noms** .

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
void DisplayGlobalAddressListForStore()
{
    Outlook.Folder currentFolder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store currentStore = currentFolder.Store;
    if (currentStore.ExchangeStoreType !=
        Outlook.OlExchangeStoreType.olNotExchange)
    {
        Outlook.SelectNamesDialog snd = 
            Application.Session.GetSelectNamesDialog();
        Outlook.AddressList addrList = 
            GetGlobalAddressList(currentStore);
        if (addrList != null)
        {
            snd.InitialAddressList = addrList;
            snd.Display();
        }
    }
}

public Outlook.AddressList GetGlobalAddressList(Outlook.Store store)
{
    string  PR_EMSMDB_SECTION_UID = 
        @"http://schemas.microsoft.com/mapi/proptag/0x3D150102";
    if (store == null)
    {
        throw new ArgumentNullException();
    }
    Outlook.PropertyAccessor oPAStore = store.PropertyAccessor;
    string storeUID = oPAStore.BinaryToString(
        oPAStore.GetProperty(PR_EMSMDB_SECTION_UID));
    foreach (Outlook.AddressList addrList 
        in Application.Session.AddressLists)
    {
        Outlook.PropertyAccessor oPAAddrList = 
            addrList.PropertyAccessor;
        string addrListUID = oPAAddrList.BinaryToString(
            oPAAddrList.GetProperty(PR_EMSMDB_SECTION_UID));
        // Return addrList if match on storeUID
        // and type is olExchangeGlobalAddressList.
        if (addrListUID == storeUID && addrList.AddressListType ==
            Outlook.OlAddressListType.olExchangeGlobalAddressList)
        {
            return addrList;
        }
    }
    return null;
}
```

Le deuxième exemple de code contient la méthode EnumerateAddressListsForStore et la fonction GetAddressLists. La méthode EnumerateAddressListsForStore affiche le type et l'ordre de résolution de chaque liste d'adresses définie pour le magasin actif. La méthode EnumerateAddressListsForStore commence par obtenir le magasin actif, puis appelle la fonction GetAddressLists pour obtenir un objet de [liste\<.NET Framework générique \>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?redirectedfrom=MSDN&view=netframework-4.8)qui contient les objets AddressList du magasin actif. 

GetAddressLists énumère chacune des listes d'adresses définies de la session et utilise l'objet PropertyAccessor ainsi que la propriété MAPI nomméehttps://schemas.microsoft.com/mapi/proptag/0x3D150102 pour obtenir la propriété PR\_EMSMDB\_SECTION\_UID d'une liste d'adresses et la propriété PR\_EMSMDB\_SECTION\_UID d'un magasin actif. GetGlobalAddressLis identifie une liste d'adresses comme étant associée à un magasin si leurs propriétés PR\_EMSMDB\_SECTION\_UID correspondent et retourne un ensemble de listes d'adresses pour le magasin actif. EnumerateAddressListsForStore utilise ensuite les propriétés [AddressListType](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist.addresslisttype?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_AddressList_AddressListType)et les propriétés[ResolutionOrder](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.addresslist.resolutionorder?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_AddressList_ResolutionOrder)de l'objet **AddressList **pour afficher le type et l'ordre de résolution de chaque liste d'adresses retournée.


```csharp
private void EnumerateAddressListsForStore()
{
    Outlook.Folder currentFolder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store currentStore = currentFolder.Store;
    List<Outlook.AddressList> addrListsForStore = 
        GetAddressLists(currentStore);
    foreach (Outlook.AddressList addrList in addrListsForStore)
    {
        Debug.WriteLine(addrList.Name 
            + " " + addrList.AddressListType.ToString()
            + " Resolution Order: " +
            addrList.ResolutionOrder);
    }
}
public List<Outlook.AddressList> GetAddressLists(Outlook.Store store)
{
    List<Outlook.AddressList> addrLists = 
        new List<Microsoft.Office.Interop.Outlook.AddressList>();
    string PR_EMSMDB_SECTION_UID =
        @"http://schemas.microsoft.com/mapi/proptag/0x3D150102";
    if (store == null)
    {
        throw new ArgumentNullException();
    }
    Outlook.PropertyAccessor oPAStore = store.PropertyAccessor;
    string storeUID = oPAStore.BinaryToString(
        oPAStore.GetProperty(PR_EMSMDB_SECTION_UID));
    foreach (Outlook.AddressList addrList
        in Application.Session.AddressLists)
    {
        Outlook.PropertyAccessor oPAAddrList =
            addrList.PropertyAccessor;
        string addrListUID = oPAAddrList.BinaryToString(
            oPAAddrList.GetProperty(PR_EMSMDB_SECTION_UID));
        // Return addrList if match on storeUID
        // and type is olExchangeGlobalAddressList.
        if (addrListUID == storeUID)
        {
            addrLists.Add(addrList);
        }
    }
    return addrLists;
}
```

## <a name="see-also"></a>Voir aussi

- [Carnet d’adresses](address-book.md)

