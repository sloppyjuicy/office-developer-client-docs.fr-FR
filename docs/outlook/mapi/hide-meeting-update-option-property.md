---
title: Hide Meeting Update Option, propriété
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ac7c891fa05560231a257f9bd52ccbbfe564b49d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412099"
---
# <a name="hide-meeting-update-option-property"></a><span data-ttu-id="2bc19-103">Hide Meeting Update Option, propriété</span><span class="sxs-lookup"><span data-stu-id="2bc19-103">Hide Meeting Update Option Property</span></span>

  
  
<span data-ttu-id="2bc19-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2bc19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2bc19-105">Masque l’option d’envoi de mises à jour de réunion aux participants ajoutés ou supprimés uniquement.</span><span class="sxs-lookup"><span data-stu-id="2bc19-105">Hides the option to send meeting updates to only added or deleted attendees.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2bc19-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="2bc19-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2bc19-107">Exposé sur :</span><span class="sxs-lookup"><span data-stu-id="2bc19-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="2bc19-108">[IMsgStore : objet IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="2bc19-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="2bc19-109">Créé par :</span><span class="sxs-lookup"><span data-stu-id="2bc19-109">Created by:</span></span>  <br/> |<span data-ttu-id="2bc19-110">Fournisseur du Store</span><span class="sxs-lookup"><span data-stu-id="2bc19-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="2bc19-111">Accessible par :</span><span class="sxs-lookup"><span data-stu-id="2bc19-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="2bc19-112">Outlook clients et autres clients</span><span class="sxs-lookup"><span data-stu-id="2bc19-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="2bc19-113">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="2bc19-113">Property type:</span></span>  <br/> |<span data-ttu-id="2bc19-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2bc19-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2bc19-115">Type d’accès :</span><span class="sxs-lookup"><span data-stu-id="2bc19-115">Access type:</span></span>  <br/> |<span data-ttu-id="2bc19-116">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2bc19-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2bc19-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="2bc19-117">Remarks</span></span>

<span data-ttu-id="2bc19-118">Pour fournir l’une des fonctionnalités du magasin, le fournisseur de magasin doit implémenter [IMAPIProp : IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour l’une de ces propriétés transmises à un appel [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="2bc19-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="2bc19-119">Lorsque la balise de propriété pour l’une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de magasin doit également renvoyer la valeur de propriété correcte.</span><span class="sxs-lookup"><span data-stu-id="2bc19-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="2bc19-120">Les fournisseurs du Store peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2bc19-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="2bc19-121">Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="2bc19-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="2bc19-122">Lorsque vous appelez [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md)spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d’entrée  _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="2bc19-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2bc19-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="2bc19-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="2bc19-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="2bc19-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="2bc19-125">ulKind :</span><span class="sxs-lookup"><span data-stu-id="2bc19-125">ulKind:</span></span>  <br/> |<span data-ttu-id="2bc19-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="2bc19-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="2bc19-127">Kind.lpwstrName :</span><span class="sxs-lookup"><span data-stu-id="2bc19-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="2bc19-128">L"urn:schemas-microsoft-com:office:outlook#allonemtgupdatedlg »</span><span class="sxs-lookup"><span data-stu-id="2bc19-128">L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"</span></span>  <br/> |
   
<span data-ttu-id="2bc19-129">Un fournisseur de magasins qui utilise un serveur pour envoyer des mises à jour de réunion peut modifier la boîte de dialogue Envoyer la mise à jour aux **participants.**</span><span class="sxs-lookup"><span data-stu-id="2bc19-129">A store provider that uses a server to send meeting updates can modify the **Send Update to Attendees** dialog box.</span></span> <span data-ttu-id="2bc19-130">Cette fonctionnalité est utile car lorsque le serveur envoie une mise à jour de réunion, le serveur ne sait pas quels participants ont été ajoutés ou supprimés par l’utilisateur depuis la demande de réunion initiale.</span><span class="sxs-lookup"><span data-stu-id="2bc19-130">This functionality is useful because when the server sends a meeting update, the server does not know which attendees have been added or deleted by the user since the initial meeting request.</span></span> <span data-ttu-id="2bc19-131">Lorsque cette propriété est **true,** l’option Envoyer uniquement aux participants ajoutés ou **supprimés** n’est pas affichée dans la boîte de dialogue Envoyer la mise à jour aux **participants.**</span><span class="sxs-lookup"><span data-stu-id="2bc19-131">When this property is **true**, the **Send update only to added or deleted attendees** option is not displayed in the **Send Update to Attendees** dialog box.</span></span> 
  
<span data-ttu-id="2bc19-132">Cette propriété est ignorée si la version de Outlook est antérieure à Microsoft Office Outlook 2003 Service Pack 1, ou si sa valeur est **false**.</span><span class="sxs-lookup"><span data-stu-id="2bc19-132">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

