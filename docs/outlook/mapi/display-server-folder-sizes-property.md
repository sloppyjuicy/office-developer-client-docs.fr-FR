---
title: Propriété d'affichage des tailles de dossier du serveur
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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 85a8b5216eac1dd4e4cebd1313cb31c9b5d70227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337078"
---
# <a name="display-server-folder-sizes-property"></a><span data-ttu-id="698b9-103">Propriété d'affichage des tailles de dossier du serveur</span><span class="sxs-lookup"><span data-stu-id="698b9-103">Display Server Folder Sizes Property</span></span>

  
  
<span data-ttu-id="698b9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="698b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="698b9-105">Affiche les tailles des dossiers spécifiés sur le serveur dans la boîte de dialogue **taille du dossier** Outlook.</span><span class="sxs-lookup"><span data-stu-id="698b9-105">Displays the sizes of specified folders on the server in the Outlook **Folder Size** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="698b9-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="698b9-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="698b9-107">Exposé sur:</span><span class="sxs-lookup"><span data-stu-id="698b9-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="698b9-108">[IMsgStore: objet IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="698b9-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="698b9-109">Créé par:</span><span class="sxs-lookup"><span data-stu-id="698b9-109">Created by:</span></span>  <br/> |<span data-ttu-id="698b9-110">Fournisseur de magasin</span><span class="sxs-lookup"><span data-stu-id="698b9-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="698b9-111">Accès par:</span><span class="sxs-lookup"><span data-stu-id="698b9-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="698b9-112">Outlook et d'autres clients</span><span class="sxs-lookup"><span data-stu-id="698b9-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="698b9-113">Type de propriété:</span><span class="sxs-lookup"><span data-stu-id="698b9-113">Property type:</span></span>  <br/> |<span data-ttu-id="698b9-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="698b9-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="698b9-115">Type d'accès:</span><span class="sxs-lookup"><span data-stu-id="698b9-115">Access type:</span></span>  <br/> |<span data-ttu-id="698b9-116">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="698b9-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="698b9-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="698b9-117">Remarks</span></span>

<span data-ttu-id="698b9-118">Pour fournir l'une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMAPIProp: IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour l'une des propriétés transmises à un appel [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="698b9-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="698b9-119">Lorsque la balise de propriété de l'une de ces propriétés est transmise à [IMAPIProp:: GetProps](imapiprop-getprops.md), le fournisseur Store doit également renvoyer la valeur de propriété correcte.</span><span class="sxs-lookup"><span data-stu-id="698b9-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="698b9-120">Les fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="698b9-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="698b9-121">Pour récupérer la valeur de cette propriété, le client doit d'abord utiliser [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp:: GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="698b9-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="698b9-122">Lors de l'appel de [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d'entrée _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="698b9-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="698b9-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="698b9-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="698b9-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="698b9-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="698b9-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="698b9-125">ulKind:</span></span>  <br/> |<span data-ttu-id="698b9-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="698b9-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="698b9-127">Kind. lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="698b9-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="698b9-128">L "urn: schemas-microsoft-com: Office: Outlook # serverfoldersizes"</span><span class="sxs-lookup"><span data-stu-id="698b9-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span></span>  <br/> |
   
<span data-ttu-id="698b9-129">Cette propriété est prise en charge dans Microsoft Outlook 2003 Service Pack (SP) 1.</span><span class="sxs-lookup"><span data-stu-id="698b9-129">This property is supported in Microsoft Outlook 2003 Service Pack (SP) 1.</span></span> <span data-ttu-id="698b9-130">Si la version d'Outlook est antérieure à Outlook 2003 SP 1, ou si sa valeur est **false**, Outlook affiche uniquement la taille des dossiers sur le magasin local.</span><span class="sxs-lookup"><span data-stu-id="698b9-130">If the version of Outlook is earlier than Outlook 2003 SP 1, or if its value is **false**, Outlook will display only the sizes of folders on the local store.</span></span> <span data-ttu-id="698b9-131">Si cette propriété est définie sur un magasin qui utilise Outlook 2003 SP 1, Outlook demande la taille de chaque dossier spécifié sur le serveur et sur le lecteur local.</span><span class="sxs-lookup"><span data-stu-id="698b9-131">If this property is set on a store that uses Outlook 2003 SP 1, Outlook will query for the size of each specified folder on the server and the local drive.</span></span> 
  
<span data-ttu-id="698b9-132">Pour rechercher la taille du dossier sur le serveur, Outlook ouvre un dossier sur le magasin avec [IMsgStore:: OpenEntry](imsgstore-openentry.md), en transmettant l'indicateur **MAPI_NO_CACHE**, puis il interroge **PR_MESSAGE_SIZE_EXTENDED**.</span><span class="sxs-lookup"><span data-stu-id="698b9-132">To query for the folder size on the server, Outlook opens a folder on the store with [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the flag **MAPI_NO_CACHE**, and then it queries for **PR_MESSAGE_SIZE_EXTENDED**.</span></span> <span data-ttu-id="698b9-133">Le fournisseur de banque doit ensuite renvoyer la taille du dossier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="698b9-133">The store provider should then return the folder size on the server.</span></span>
  
<span data-ttu-id="698b9-134">Pour rechercher la taille d'un dossier sur le lecteur local, Outlook ouvre le dossier sans l'indicateur **MAPI_NO_CACHE** .</span><span class="sxs-lookup"><span data-stu-id="698b9-134">To query for the size of a folder on the local drive, Outlook opens the folder without the **MAPI_NO_CACHE** flag.</span></span> <span data-ttu-id="698b9-135">Il interroge ensuite **PR_MESSAGE_SIZE_EXTENDED**; le fournisseur de la Banque doit renvoyer la taille du dossier spécifié sur le lecteur local.</span><span class="sxs-lookup"><span data-stu-id="698b9-135">It then queries for **PR_MESSAGE_SIZE_EXTENDED**; the store provider should return the size of the specified folder on the local drive.</span></span>
  
<span data-ttu-id="698b9-136">Avec ce jeu de propriétés, les fournisseurs de magasin qui synchronisent le contenu du magasin sur un serveur peuvent afficher les données de taille de dossier sur le serveur dans la boîte de dialogue **taille du dossier** Outlook.</span><span class="sxs-lookup"><span data-stu-id="698b9-136">With this property set, store providers that synchronize store contents to a server can display folder size data on the server in the Outlook **Folder Size** dialog box.</span></span> <span data-ttu-id="698b9-137">Les utilisateurs peuvent ensuite comparer leur utilisation de stockage de serveur actuelle avec des quotas de serveur.</span><span class="sxs-lookup"><span data-stu-id="698b9-137">Users can then compare their current server storage usage with server quotas.</span></span> 
  

