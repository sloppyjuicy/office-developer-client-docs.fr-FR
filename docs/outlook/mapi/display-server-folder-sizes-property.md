---
title: Propriété d’affichage des tailles de dossier du serveur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Display Server Folder Sizes Property
api_type:
- COM
ms.assetid: 38429fdb-be93-213a-a780-80f9837f55fa
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f1ec10bde39f853a80540b48216478edc4e41f12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584309"
---
# <a name="display-server-folder-sizes-property"></a><span data-ttu-id="7dcc1-103">Propriété d’affichage des tailles de dossier du serveur</span><span class="sxs-lookup"><span data-stu-id="7dcc1-103">Display Server Folder Sizes Property</span></span>

  
  
<span data-ttu-id="7dcc1-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7dcc1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7dcc1-105">Affiche la taille des dossiers spécifiés sur le serveur dans la boîte de dialogue Outlook **Taille du dossier** .</span><span class="sxs-lookup"><span data-stu-id="7dcc1-105">Displays the sizes of specified folders on the server in the Outlook **Folder Size** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7dcc1-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7dcc1-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7dcc1-107">Exposée sur :</span><span class="sxs-lookup"><span data-stu-id="7dcc1-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="7dcc1-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) objet</span><span class="sxs-lookup"><span data-stu-id="7dcc1-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="7dcc1-109">Créé par :</span><span class="sxs-lookup"><span data-stu-id="7dcc1-109">Created by:</span></span>  <br/> |<span data-ttu-id="7dcc1-110">Fournisseur de banque</span><span class="sxs-lookup"><span data-stu-id="7dcc1-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="7dcc1-111">Accessible par :</span><span class="sxs-lookup"><span data-stu-id="7dcc1-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="7dcc1-112">Outlook et autres clients</span><span class="sxs-lookup"><span data-stu-id="7dcc1-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="7dcc1-113">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="7dcc1-113">Property type:</span></span>  <br/> |<span data-ttu-id="7dcc1-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7dcc1-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7dcc1-115">Type d’accès :</span><span class="sxs-lookup"><span data-stu-id="7dcc1-115">Access type:</span></span>  <br/> |<span data-ttu-id="7dcc1-116">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7dcc1-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="7dcc1-117">Remarks</span></span>

<span data-ttu-id="7dcc1-118">Pour fournir une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMAPIProp : IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour une de ces propriétés passées à un appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="7dcc1-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="7dcc1-119">Lorsque la balise de propriété pour une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de banque doit également retourner la valeur de la propriété adéquate.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="7dcc1-120">Fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="7dcc1-121">Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifiez cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="7dcc1-122">Lors de l’appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) sur laquelle pointé le paramètre d’entrée _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="7dcc1-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7dcc1-123">lpGuid :</span><span class="sxs-lookup"><span data-stu-id="7dcc1-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="7dcc1-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="7dcc1-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="7dcc1-125">ulKind :</span><span class="sxs-lookup"><span data-stu-id="7dcc1-125">ulKind:</span></span>  <br/> |<span data-ttu-id="7dcc1-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="7dcc1-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="7dcc1-127">Kind.lpwstrName :</span><span class="sxs-lookup"><span data-stu-id="7dcc1-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="7dcc1-128">L « urn : schemas-microsoft-com:office:outlook #serverfoldersizes »</span><span class="sxs-lookup"><span data-stu-id="7dcc1-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span></span>  <br/> |
   
<span data-ttu-id="7dcc1-129">Cette propriété est prise en charge dans Microsoft Outlook 2003 Service Pack (SP) 1.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-129">This property is supported in Microsoft Outlook 2003 Service Pack (SP) 1.</span></span> <span data-ttu-id="7dcc1-130">Si la version d’Outlook est antérieure à Outlook 2003 Service Pack 1, ou si sa valeur est **false**, Outlook affiche uniquement les tailles des dossiers dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-130">If the version of Outlook is earlier than Outlook 2003 SP 1, or if its value is **false**, Outlook will display only the sizes of folders on the local store.</span></span> <span data-ttu-id="7dcc1-131">Si cette propriété est définie sur un magasin qui utilise Outlook 2003 Service Pack 1, Outlook interroge la taille de chaque dossier spécifié sur le serveur et le disque local.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-131">If this property is set on a store that uses Outlook 2003 SP 1, Outlook will query for the size of each specified folder on the server and the local drive.</span></span> 
  
<span data-ttu-id="7dcc1-132">Pour rechercher la taille du dossier sur le serveur, Outlook ouvre un dossier sur le magasin avec [IMsgStore::OpenEntry](imsgstore-openentry.md), en passant l’indicateur **MAPI_NO_CACHE**, et il interroge pour **PR_MESSAGE_SIZE_EXTENDED**.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-132">To query for the folder size on the server, Outlook opens a folder on the store with [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the flag **MAPI_NO_CACHE**, and then it queries for **PR_MESSAGE_SIZE_EXTENDED**.</span></span> <span data-ttu-id="7dcc1-133">Le fournisseur de banque doit ensuite retourner la taille du dossier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-133">The store provider should then return the folder size on the server.</span></span>
  
<span data-ttu-id="7dcc1-134">Pour rechercher la taille d’un dossier sur le disque local, Outlook ouvre le dossier sans l’indicateur **MAPI_NO_CACHE** .</span><span class="sxs-lookup"><span data-stu-id="7dcc1-134">To query for the size of a folder on the local drive, Outlook opens the folder without the **MAPI_NO_CACHE** flag.</span></span> <span data-ttu-id="7dcc1-135">Il interroge **PR_MESSAGE_SIZE_EXTENDED**; ensuite le fournisseur de banque doit renvoyer la taille du dossier spécifié sur le disque local.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-135">It then queries for **PR_MESSAGE_SIZE_EXTENDED**; the store provider should return the size of the specified folder on the local drive.</span></span>
  
<span data-ttu-id="7dcc1-136">Avec ce jeu de propriétés, les fournisseurs de magasins synchroniser le magasin de contenu vers un serveur peuvent afficher des données de taille de dossier sur le serveur dans la boîte de dialogue Outlook **Taille du dossier** .</span><span class="sxs-lookup"><span data-stu-id="7dcc1-136">With this property set, store providers that synchronize store contents to a server can display folder size data on the server in the Outlook **Folder Size** dialog box.</span></span> <span data-ttu-id="7dcc1-137">Les utilisateurs peuvent comparer puis leur utilisation actuelle de stockage serveur avec des quotas de serveur.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-137">Users can then compare their current server storage usage with server quotas.</span></span> 
  

