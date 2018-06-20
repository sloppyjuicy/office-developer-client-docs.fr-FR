---
title: Masquer la propriété de Option de mise à jour de réunion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Hide Meeting Update Option Property
api_type:
- COM
ms.assetid: 9e7b413f-a88a-a4ec-8d57-1f3058cce4a4
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 25942df6f6156266f16cf6e681270dbb530472e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783453"
---
# <a name="hide-meeting-update-option-property"></a><span data-ttu-id="d4e09-103">Masquer la propriété de Option de mise à jour de réunion</span><span class="sxs-lookup"><span data-stu-id="d4e09-103">Hide Meeting Update Option Property</span></span>

  
  
<span data-ttu-id="d4e09-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4e09-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4e09-105">Masque l’option Envoyer des mises à jour de réunion pour seulement les participants ajoutés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="d4e09-105">Hides the option to send meeting updates to only added or deleted attendees.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d4e09-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="d4e09-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4e09-107">Exposée sur :</span><span class="sxs-lookup"><span data-stu-id="d4e09-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="d4e09-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) objet</span><span class="sxs-lookup"><span data-stu-id="d4e09-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="d4e09-109">Créé par :</span><span class="sxs-lookup"><span data-stu-id="d4e09-109">Created by:</span></span>  <br/> |<span data-ttu-id="d4e09-110">Fournisseur de banque</span><span class="sxs-lookup"><span data-stu-id="d4e09-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="d4e09-111">Accessible par :</span><span class="sxs-lookup"><span data-stu-id="d4e09-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="d4e09-112">Outlook et autres clients</span><span class="sxs-lookup"><span data-stu-id="d4e09-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="d4e09-113">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="d4e09-113">Property type:</span></span>  <br/> |<span data-ttu-id="d4e09-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d4e09-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d4e09-115">Type d’accès :</span><span class="sxs-lookup"><span data-stu-id="d4e09-115">Access type:</span></span>  <br/> |<span data-ttu-id="d4e09-116">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="d4e09-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4e09-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="d4e09-117">Remarks</span></span>

<span data-ttu-id="d4e09-118">Pour fournir une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMAPIProp : IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour une de ces propriétés passées à un appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="d4e09-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="d4e09-119">Lorsque la balise de propriété pour une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de banque doit également retourner la valeur de la propriété adéquate.</span><span class="sxs-lookup"><span data-stu-id="d4e09-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="d4e09-120">Fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d4e09-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="d4e09-121">Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifiez cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="d4e09-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="d4e09-122">Lors de l’appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) sur laquelle pointé le paramètre d’entrée _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="d4e09-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d4e09-123">lpGuid :</span><span class="sxs-lookup"><span data-stu-id="d4e09-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="d4e09-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="d4e09-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="d4e09-125">ulKind :</span><span class="sxs-lookup"><span data-stu-id="d4e09-125">ulKind:</span></span>  <br/> |<span data-ttu-id="d4e09-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="d4e09-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="d4e09-127">Kind.lpwstrName :</span><span class="sxs-lookup"><span data-stu-id="d4e09-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="d4e09-128">L « urn : schemas-microsoft-com:office:outlook #allornonemtgupdatedlg »</span><span class="sxs-lookup"><span data-stu-id="d4e09-128">L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"</span></span>  <br/> |
   
<span data-ttu-id="d4e09-129">Un fournisseur de magasins qui utilise un serveur pour envoyer des mises à jour de réunion permettre modifier la boîte de dialogue **Envoyer la mise à jour aux participants** .</span><span class="sxs-lookup"><span data-stu-id="d4e09-129">A store provider that uses a server to send meeting updates can modify the **Send Update to Attendees** dialog box.</span></span> <span data-ttu-id="d4e09-130">Cette fonctionnalité est utile car lorsque le serveur envoie une mise à jour de la réunion, le serveur ne sait pas les participants ont été ajoutés ou supprimés par l’utilisateur par rapport à la demande de réunion initiale.</span><span class="sxs-lookup"><span data-stu-id="d4e09-130">This functionality is useful because when the server sends a meeting update, the server does not know which attendees have been added or deleted by the user since the initial meeting request.</span></span> <span data-ttu-id="d4e09-131">Lorsque cette propriété a la **valeur true**, l’option **Envoyer des mises à jour uniquement aux participants ajoutés ou supprimés** s’affiche pas dans la boîte de dialogue **Envoyer la mise à jour aux participants** .</span><span class="sxs-lookup"><span data-stu-id="d4e09-131">When this property is **true**, the **Send update only to added or deleted attendees** option is not displayed in the **Send Update to Attendees** dialog box.</span></span> 
  
<span data-ttu-id="d4e09-132">Cette propriété est ignorée si la version d’Outlook est antérieure à Microsoft Office Outlook 2003 Service Pack 1, ou si sa valeur est **false**.</span><span class="sxs-lookup"><span data-stu-id="d4e09-132">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

