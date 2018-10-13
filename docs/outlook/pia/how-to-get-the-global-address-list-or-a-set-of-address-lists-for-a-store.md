---
title: Obtenir la Liste d’Adresses Globale ou d’un ensemble de listes d’adresses pour un magasin
TOCTitle: Get the Global Address List or a set of address lists for a store
ms:assetid: a361ac58-25c6-4ce1-97b0-403ad67ee7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184631(v=office.15)
ms:contentKeyID: 55119800
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b27c6c6fd9cf70a691f4a2df628a342cf024d8d6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406455"
---
# <a name="get-the-global-address-list-or-a-set-of-address-lists-for-a-store"></a><span data-ttu-id="ef6e1-102">Obtenir la Liste d’Adresses Globale ou d’un ensemble de listes d’adresses pour un magasin</span><span class="sxs-lookup"><span data-stu-id="ef6e1-102">Get the Global Address List or a set of address lists for a store</span></span>

<span data-ttu-id="ef6e1-103">Cette rubrique contient deux exemples de code qui montrent comment obtenir la liste d'adresses globale associée à un magasin et comment obtenir toutes les listes d'adresses associées à un magasin.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-103">This topic contains two code examples that show how to get the Global Address List (GAL) that is associated with a store, and how to get all of the address lists that are associated with a store.</span></span>

## <a name="example"></a><span data-ttu-id="ef6e1-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="ef6e1-104">Example</span></span>

<span data-ttu-id="ef6e1-105">Dans une session Microsoft Outlook où plusieurs comptes Microsoft Exchange sont définis dans le profil, plusieurs listes d'adresses peuvent être associées à un magasin.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-105">In a Microsoft Outlook session where multiple Microsoft Exchange accounts are defined in the profile, there can be multiple address lists associated with a store.</span></span> <span data-ttu-id="ef6e1-106">Dans chacun des exemples de code suivants, le magasin spécifique qui nous intéresse est le magasin du dossier actif affiché dans l'explorateur actif, mais l'algorithme permettant d'obtenir une liste d'adresses globale ou un ensemble d'objets [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) pour un magasin s'applique à n'importe quel magasin Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-106">In each of the following code examples, the specific store of interest is the store for the current folder displayed in the active explorer, but the algorithm to get a Global Address List or a set of [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) objects for a store applies to any Exchange store.</span></span>

<span data-ttu-id="ef6e1-107">Le premier exemple de code contient la méthode DisplayGlobalAddressListForStore ainsi que la fonction GetGlobalAddressList.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-107">The first code example contains the   method and the   function.</span></span> <span data-ttu-id="ef6e1-108">La méthode DisplayGlobalAddressListForStore affiche, dans la boîte de dialogue**Sélectionner des Noms**, la Liste d'adresses Globale associée au magasin actuel.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-108">The   method displays, in the Select Names dialog box, the Global Address List that is associated with the current store.</span></span> <span data-ttu-id="ef6e1-109">DisplayGlobalAddressListForStore obtient d’abord le magasin actif.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-109"> first obtains the current store.</span></span> <span data-ttu-id="ef6e1-110">S'il s'agit d'un magasin Exchange, la fonction GetGlobalAddressList est appelée pour obtenir la Liste d'Adresses Globale associée au magasin actif.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-110">If the current store is an Exchange store,   is called to obtain the Global Address List associated with the current store.</span></span> 

<span data-ttu-id="ef6e1-111">GetGlobalAddressList utilise l'objet [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) et la propriété MAPIhttps://schemas.microsoft.com/mapi/proptag/0x3D150102pour obtenir la propriété PR\_EMSMDB\_SECTION\_UID d'une liste d'adresses et du magasin actif.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-111"> uses the PropertyAccessor object and the MAPI property   to obtain the PR_EMSMDB_SECTION_UID property of an address list and the current store.</span></span> <span data-ttu-id="ef6e1-112">GetGlobalAddressList identifie une liste d'adresses comme étant associée à un magasin si leurs propriétés PR\_EMSMDB\_SECTION\_UID correspondent, et si la liste d'adresses est la Liste d'Adresses Globale si sa propriété [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) a la valeur [olExchangeGlobalAddressList](https://msdn.microsoft.com/library/bb644009\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ef6e1-112"> identifies an address list as associated with a store if their PR_EMSMDB_SECTION_UID properties match, and the address list is the Global Address List if its AddressListType property is olExchangeGlobalAddressList .</span></span> <span data-ttu-id="ef6e1-113">Si l'appel à la fonction réussit, DisplayGlobalAddressListForStore   utilise l'objet[SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\))pour afficher la Liste d'Adresses Globale retournée dans la boîte de dialogue**Sélectionner des Noms**.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-113">If the call to   succeeds,   uses the SelectNamesDialog object to display the returned Global Address List in the Select Names dialog box.</span></span>

<span data-ttu-id="ef6e1-114">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d'abord ajouter une référence au composant Bibliothèque d'objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l'espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="ef6e1-115">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-115">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="ef6e1-116">La ligne de code suivante montre comment effectuer l'importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-116">The following line of code shows how to do the import and assignment in C#.</span></span>

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
        @"https://schemas.microsoft.com/mapi/proptag/0x3D150102";
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

<span data-ttu-id="ef6e1-117">Le deuxième exemple de code contient la méthode EnumerateAddressListsForStore et la fonction GetAddressLists.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-117">The second code example contains the   method and   function.</span></span> <span data-ttu-id="ef6e1-118">La méthode EnumerateAddressListsForStore affiche le type et l'ordre de résolution de chaque liste d'adresses définie pour le magasin actif.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-118">The   method displays the type and resolution order of each address list defined for the current store.</span></span> <span data-ttu-id="ef6e1-119">La méthode EnumerateAddressListsForStore commence par obtenir le magasin actif, puis appelle la fonction GetAddressLists pour obtenir un objet de [liste\<.NET Framework générique \>](https://msdn.microsoft.com/fr-FR/library/6sh2ey19)qui contient les objets AddressList du magasin actif.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-119"> first obtains the current store, and then calls   to obtain a .NET Framework generic ListT  object that contains AddressList objects for the current store.</span></span> 

<span data-ttu-id="ef6e1-120">GetAddressLists énumère chacune des listes d'adresses définies de la session et utilise l'objet PropertyAccessor ainsi que la propriété MAPI nomméehttps://schemas.microsoft.com/mapi/proptag/0x3D150102 pour obtenir la propriété PR\_EMSMDB\_SECTION\_UID d'une liste d'adresses et la propriété PR\_EMSMDB\_SECTION\_UID d'un magasin actif.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-120"> enumerates each address list defined for the session, uses the PropertyAccessor object and the MAPI named property   to obtain the PR_EMSMDB_SECTION_UID property of an address list, and the PR_EMSMDB_SECTION_UID property of a current store.</span></span> <span data-ttu-id="ef6e1-121">GetGlobalAddressLis identifie une liste d'adresses comme étant associée à un magasin si leurs propriétés PR\_EMSMDB\_SECTION\_UID correspondent et retourne un ensemble de listes d'adresses pour le magasin actif.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-121"> identifies an address list as associated with a store if their PR_EMSMDB_SECTION_UID properties match, and returns a set of address lists for the current store.</span></span> <span data-ttu-id="ef6e1-122">EnumerateAddressListsForStore utilise ensuite les propriétés [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\))et les propriétés[ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\))de l'objet \*\*AddressList \*\*pour afficher le type et l'ordre de résolution de chaque liste d'adresses retournée.</span><span class="sxs-lookup"><span data-stu-id="ef6e1-122"> then uses the AddressListType and ResolutionOrder properties of the AddressList object to display the type and resolution order for each returned address list.</span></span>

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
        @"https://schemas.microsoft.com/mapi/proptag/0x3D150102";
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

## <a name="see-also"></a><span data-ttu-id="ef6e1-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef6e1-123">See also</span></span>

- [<span data-ttu-id="ef6e1-124">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="ef6e1-124">Address Book</span></span>](address-book.md)

