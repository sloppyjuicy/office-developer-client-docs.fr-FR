---
title: Obtenir la Liste d’Adresses Globale ou d’un ensemble de listes d’adresses pour un magasin
TOCTitle: Get the Global Address List or a set of address lists for a store
ms:assetid: a361ac58-25c6-4ce1-97b0-403ad67ee7a4
ms:mtpsurl: https://learn.microsoft.com/office/client-developer/outlook/pia/how-to-get-the-global-address-list-or-a-set-of-address-lists-for-a-store
ms:contentKeyID: 55119800
ms.date: 12/03/2019
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3bbdc21fe83da32c4973512b78b835bf8846dbc1
ms.sourcegitcommit: b6d8fc4db483ecd1a3247a6cb3377f5b52c44cfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2022
ms.locfileid: "68574307"
---
# <a name="get-the-global-address-list-or-a-set-of-address-lists-for-a-store"></a>Obtenir la Liste d’Adresses Globale ou d’un ensemble de listes d’adresses pour un magasin

Cette rubrique contient deux exemples de code qui montrent comment obtenir la liste d'adresses globale associée à un magasin et comment obtenir toutes les listes d'adresses associées à un magasin.

## <a name="example"></a>Exemple

Dans une session Microsoft Outlook où plusieurs comptes Microsoft Exchange sont définis dans le profil, plusieurs listes d'adresses peuvent être associées à un magasin. Dans chacun des exemples de code suivants, le magasin spécifique qui nous intéresse est le magasin du dossier actif affiché dans l'explorateur actif, mais l'algorithme permettant d'obtenir une liste d'adresses globale ou un ensemble d'objets [AddressList](/dotnet/api/microsoft.office.interop.outlook.addresslist) pour un magasin s'applique à n'importe quel magasin Exchange.

Le premier exemple de code contient la méthode DisplayGlobalAddressListForStore ainsi que la fonction GetGlobalAddressList. La méthode DisplayGlobalAddressListForStore affiche, dans la boîte de dialogue **Sélectionner des Noms**, la Liste d'adresses Globale associée au magasin actuel. DisplayGlobalAddressListForStore obtient d’abord le magasin actif. S'il s'agit d'un magasin Exchange, la fonction GetGlobalAddressList est appelée pour obtenir la Liste d'Adresses Globale associée au magasin actif. 

GetGlobalAddressList utilise l'objet [PropertyAccessor](/dotnet/api/microsoft.office.interop.outlook.propertyaccessor) et la propriété MAPI`https://schemas.microsoft.com/mapi/proptag/0x3D150102`pour obtenir la propriété PR\_EMSMDB\_SECTION\_UID d'une liste d'adresses et du magasin actif. GetGlobalAddressList identifie une liste d'adresses comme étant associée à un magasin si leurs propriétés PR\_EMSMDB\_SECTION\_UID correspondent, et si la liste d'adresses est la Liste d'Adresses Globale si sa propriété [AddressListType](/dotnet/api/microsoft.office.interop.outlook.addresslist.addresslisttype) a la valeur [olExchangeGlobalAddressList](/dotnet/api/microsoft.office.interop.outlook.oladdresslisttype). Si l'appel à la fonction réussit, DisplayGlobalAddressListForStore   utilise l'objet [SelectNamesDialog](/dotnet/api/microsoft.office.interop.outlook.selectnamesdialog)pour afficher la Liste d'Adresses Globale retournée dans la boîte de dialogue **Sélectionner des Noms**.

If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace. The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C\#.

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

Le deuxième exemple de code contient la méthode EnumerateAddressListsForStore et la fonction GetAddressLists. La méthode EnumerateAddressListsForStore affiche le type et l'ordre de résolution de chaque liste d'adresses définie pour le magasin actif. EnumerateAddressListsForStore obtient d’abord le magasin actuel, puis appelle GetAddressLists pour obtenir un objet [de liste\<T\>](/dotnet/api/system.collections.generic.list-1) générique .NET Framework qui contient des objets AddressList pour le magasin actuel. 

GetAddressLists énumère chacune des listes d'adresses définies de la session et utilise l'objet PropertyAccessor ainsi que la propriété MAPI nommée`https://schemas.microsoft.com/mapi/proptag/0x3D150102` pour obtenir la propriété PR\_EMSMDB\_SECTION\_UID d'une liste d'adresses et la propriété PR\_EMSMDB\_SECTION\_UID d'un magasin actif. GetGlobalAddressLis identifie une liste d'adresses comme étant associée à un magasin si leurs propriétés PR\_EMSMDB\_SECTION\_UID correspondent et retourne un ensemble de listes d'adresses pour le magasin actif. EnumerateAddressListsForStore utilise ensuite les propriétés [AddressListType](/dotnet/api/microsoft.office.interop.outlook.addresslist.addresslisttype)et les propriétés [ResolutionOrder](/dotnet/api/microsoft.office.interop.outlook.addresslist.resolutionorder)de l'objet **AddressList** pour afficher le type et l'ordre de résolution de chaque liste d'adresses retournée.

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
