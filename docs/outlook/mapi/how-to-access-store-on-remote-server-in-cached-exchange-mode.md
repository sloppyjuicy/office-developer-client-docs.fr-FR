---
title: Accéder à une banque sur le serveur distant lorsqu'Outlook est en mode Exchange mis en cache
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Dernière modification le: 02 juillet 2012'
ms.openlocfilehash: 0d977507f6aff8aa5fbf437b4b718486a71f67dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299061"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="2a573-103">Accéder à une banque sur le serveur distant lorsqu'Outlook est en mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="2a573-103">Access a store on the remote server when Outlook is in Cached Exchange Mode</span></span>
 
<span data-ttu-id="2a573-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a573-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a573-105">Cette rubrique contient un exemple de code en C++ qui montre comment utiliser l'indicateur **MAPI_NO_CACHE** pour ouvrir un dossier ou un message dans une banque de messages sur le serveur distant lorsque Microsoft Office Outlook est en mode Exchange mis en cache.</span><span class="sxs-lookup"><span data-stu-id="2a573-105">This topic contains a code sample in C++ that shows how to use the **MAPI_NO_CACHE** flag to open a folder or a message on a message store on the remote server when Microsoft Office Outlook is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="2a573-106">Le mode Exchange mis en cache permet à Outlook d'utiliser une copie locale de la boîte aux lettres d'un utilisateur pendant qu'Outlook maintient une connexion en ligne à une copie distante de la boîte aux lettres de l'utilisateur sur le serveur Exchange distant.</span><span class="sxs-lookup"><span data-stu-id="2a573-106">Cached Exchange Mode permits Outlook to use a local copy of a user's mailbox while Outlook maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="2a573-107">Lorsqu'Outlook est exécuté en mode Exchange mis en cache, par défaut, toutes les solutions MAPI qui se connectent à la même session sont également connectées à la Banque de messages mise en cache.</span><span class="sxs-lookup"><span data-stu-id="2a573-107">When Outlook is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="2a573-108">Toutes les données auxquelles un accès est effectué et toutes les modifications apportées sont effectuées par rapport à la copie locale de la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="2a573-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="2a573-109">Un client ou un fournisseur de services peut remplacer la connexion à la Banque de messages locale et ouvrir un message ou un dossier dans le magasin distant en définissant le bit pour **MAPI_NO_CACHE** dans le paramètre *ulFlags* lors de l'appel de **[IMsgStore:: OpenEntry](imsgstore-openentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="2a573-109">A client or service provider can override the connection to the local message store and open a message or a folder on the remote store by setting the bit for **MAPI_NO_CACHE** in the  *ulFlags*  parameter when calling **[IMsgStore::OpenEntry](imsgstore-openentry.md)**.</span></span> 
  
<span data-ttu-id="2a573-110">L'exemple de code suivant montre comment appeler **IMsgStore:: OpenEntry** avec l'indicateur **MAPI_NO_CACHE** défini dans le paramètre *ulFlags* pour ouvrir le dossier racine sur le magasin de messages distant.</span><span class="sxs-lookup"><span data-stu-id="2a573-110">The following code sample shows how to call **IMsgStore::OpenEntry** with the **MAPI_NO_CACHE** flag set in the  *ulFlags*  parameter to open the root folder on the remote message store.</span></span> 
  
```cpp
HRESULT HrOpenRootFolder ( 
    LPMDB lpMDB, 
    LPMESSAGE* lpRootFolder) 
{ 
    ULONG ulObjType = NULL; 
    HRESULT hRes = lpMDB-&gt;OpenEntry( 
        0,// size of entry ID       
        NULL,                                   // Pointer to entry ID 
        NULL,                                   // Use default interface (IMAPIFolder) 
        MAPI_BEST_ACCESS | MAPI_NO_CACHE,       // Flags 
        &amp;ulObjType,
// Output parameter indicates the type of object returned 
        (LPUNKNOWN *) lpRootFolder));           // Pointer to put the opened folder in 
    return hRes; 
 
}
```

<span data-ttu-id="2a573-111">Si vous avez ouvert la Banque de messages avec l'indicateur **MDB_ONLINE** sur le serveur distant, il n'est pas nécessaire d'utiliser l'indicateur **MAPI_NO_CACHE** .</span><span class="sxs-lookup"><span data-stu-id="2a573-111">If you opened the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2a573-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a573-112">See also</span></span>

- [<span data-ttu-id="2a573-113">À propos des ajouts MAPI</span><span class="sxs-lookup"><span data-stu-id="2a573-113">About MAPI Additions</span></span>](about-mapi-additions.md)
- [<span data-ttu-id="2a573-114">Ouvrir une banque sur le serveur distant lorsqu’Outlook est en mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="2a573-114">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="2a573-115">Gérer un message dans un fichier OST sans appeler de synchronisation en mode Exchange mis en cache</span><span class="sxs-lookup"><span data-stu-id="2a573-115">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

