---
title: Display Server Folder Sizes, propriété
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 85a8b5216eac1dd4e4cebd1313cb31c9b5d70227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434549"
---
# <a name="display-server-folder-sizes-property"></a><span data-ttu-id="eb7d4-103">Display Server Folder Sizes, propriété</span><span class="sxs-lookup"><span data-stu-id="eb7d4-103">Display Server Folder Sizes Property</span></span>

  
  
<span data-ttu-id="eb7d4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb7d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb7d4-105">Affiche la taille des dossiers spécifiés sur le serveur dans la boîte de dialogue Outlook **taille du** dossier.</span><span class="sxs-lookup"><span data-stu-id="eb7d4-105">Displays the sizes of specified folders on the server in the Outlook **Folder Size** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="eb7d4-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="eb7d4-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb7d4-107">Exposé sur :</span><span class="sxs-lookup"><span data-stu-id="eb7d4-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="eb7d4-108">[IMsgStore : objet IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="eb7d4-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="eb7d4-109">Créé par :</span><span class="sxs-lookup"><span data-stu-id="eb7d4-109">Created by:</span></span>  <br/> |<span data-ttu-id="eb7d4-110">Fournisseur du Store</span><span class="sxs-lookup"><span data-stu-id="eb7d4-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="eb7d4-111">Accessible par :</span><span class="sxs-lookup"><span data-stu-id="eb7d4-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="eb7d4-112">Outlook clients et autres clients</span><span class="sxs-lookup"><span data-stu-id="eb7d4-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="eb7d4-113">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="eb7d4-113">Property type:</span></span>  <br/> |<span data-ttu-id="eb7d4-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="eb7d4-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="eb7d4-115">Type d’accès :</span><span class="sxs-lookup"><span data-stu-id="eb7d4-115">Access type:</span></span>  <br/> |<span data-ttu-id="eb7d4-116">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="eb7d4-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb7d4-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="eb7d4-117">Remarks</span></span>

<span data-ttu-id="eb7d4-118">Pour fournir l’une des fonctionnalités du magasin, le fournisseur de magasin doit implémenter [IMAPIProp : IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour l’une de ces propriétés transmises à un appel [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="eb7d4-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="eb7d4-119">Lorsque la balise de propriété pour l’une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de magasin doit également renvoyer la valeur de propriété correcte.</span><span class="sxs-lookup"><span data-stu-id="eb7d4-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="eb7d4-120">Les fournisseurs du Store peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="eb7d4-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="eb7d4-121">Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="eb7d4-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="eb7d4-122">Lorsque vous appelez [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md)spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d’entrée  _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="eb7d4-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb7d4-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="eb7d4-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="eb7d4-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="eb7d4-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="eb7d4-125">ulKind :</span><span class="sxs-lookup"><span data-stu-id="eb7d4-125">ulKind:</span></span>  <br/> |<span data-ttu-id="eb7d4-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="eb7d4-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="eb7d4-127">Kind.lpwstrName :</span><span class="sxs-lookup"><span data-stu-id="eb7d4-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="eb7d4-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes »</span><span class="sxs-lookup"><span data-stu-id="eb7d4-128">L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"</span></span>  <br/> |
   
<span data-ttu-id="eb7d4-129">Cette propriété est prise en charge dans Microsoft Outlook 2003 Service Pack (SP) 1.</span><span class="sxs-lookup"><span data-stu-id="eb7d4-129">This property is supported in Microsoft Outlook 2003 Service Pack (SP) 1.</span></span> <span data-ttu-id="eb7d4-130">Si la version de Outlook est antérieure à Outlook 2003 SP 1, ou si sa valeur est **false,** Outlook affiche uniquement les tailles de dossiers sur la boutique locale.</span><span class="sxs-lookup"><span data-stu-id="eb7d4-130">If the version of Outlook is earlier than Outlook 2003 SP 1, or if its value is **false**, Outlook will display only the sizes of folders on the local store.</span></span> <span data-ttu-id="eb7d4-131">Si cette propriété est définie sur un magasin qui utilise Outlook 2003 SP 1, Outlook interrogera la taille de chaque dossier spécifié sur le serveur et le lecteur local.</span><span class="sxs-lookup"><span data-stu-id="eb7d4-131">If this property is set on a store that uses Outlook 2003 SP 1, Outlook will query for the size of each specified folder on the server and the local drive.</span></span> 
  
<span data-ttu-id="eb7d4-132">Pour interroger la taille du dossier sur le serveur, Outlook ouvre un dossier dans la boutique avec [IMsgStore::OpenEntry](imsgstore-openentry.md), en passant l’indicateur **MAPI_NO_CACHE**, puis il interroge **PR_MESSAGE_SIZE_EXTENDED**.</span><span class="sxs-lookup"><span data-stu-id="eb7d4-132">To query for the folder size on the server, Outlook opens a folder on the store with [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the flag **MAPI_NO_CACHE**, and then it queries for **PR_MESSAGE_SIZE_EXTENDED**.</span></span> <span data-ttu-id="eb7d4-133">Le fournisseur de magasins doit ensuite renvoyer la taille du dossier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="eb7d4-133">The store provider should then return the folder size on the server.</span></span>
  
<span data-ttu-id="eb7d4-134">Pour interroger la taille d’un dossier sur le lecteur local, Outlook ouvre le dossier sans **l’indicateur MAPI_NO_CACHE'**</span><span class="sxs-lookup"><span data-stu-id="eb7d4-134">To query for the size of a folder on the local drive, Outlook opens the folder without the **MAPI_NO_CACHE** flag.</span></span> <span data-ttu-id="eb7d4-135">Il interroge ensuite **PR_MESSAGE_SIZE_EXTENDED**; Le fournisseur de magasins doit renvoyer la taille du dossier spécifié sur le lecteur local.</span><span class="sxs-lookup"><span data-stu-id="eb7d4-135">It then queries for **PR_MESSAGE_SIZE_EXTENDED**; the store provider should return the size of the specified folder on the local drive.</span></span>
  
<span data-ttu-id="eb7d4-136">Avec cette propriété définie, les fournisseurs de magasins qui synchronisent le contenu du magasin avec un serveur peuvent afficher les données de taille de dossier sur le serveur dans la boîte de dialogue taille Outlook **dossier.**</span><span class="sxs-lookup"><span data-stu-id="eb7d4-136">With this property set, store providers that synchronize store contents to a server can display folder size data on the server in the Outlook **Folder Size** dialog box.</span></span> <span data-ttu-id="eb7d4-137">Les utilisateurs peuvent ensuite comparer leur utilisation actuelle du stockage du serveur avec les quotas de serveur.</span><span class="sxs-lookup"><span data-stu-id="eb7d4-137">Users can then compare their current server storage usage with server quotas.</span></span> 
  

