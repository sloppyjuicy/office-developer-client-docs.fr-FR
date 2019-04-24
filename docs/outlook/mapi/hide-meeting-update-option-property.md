---
title: Masquer la propriété d'option de mise à jour de réunion
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
ms.openlocfilehash: ac7c891fa05560231a257f9bd52ccbbfe564b49d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299509"
---
# <a name="hide-meeting-update-option-property"></a><span data-ttu-id="f0a20-103">Masquer la propriété d'option de mise à jour de réunion</span><span class="sxs-lookup"><span data-stu-id="f0a20-103">Hide Meeting Update Option Property</span></span>

  
  
<span data-ttu-id="f0a20-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0a20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0a20-105">Masque l'option permettant d'envoyer des mises à jour de réunion uniquement aux participants ajoutés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="f0a20-105">Hides the option to send meeting updates to only added or deleted attendees.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f0a20-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="f0a20-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0a20-107">Exposé sur:</span><span class="sxs-lookup"><span data-stu-id="f0a20-107">Exposed on:</span></span>  <br/> |<span data-ttu-id="f0a20-108">[IMsgStore: objet IMAPIProp](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="f0a20-108">[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) object</span></span>  <br/> |
|<span data-ttu-id="f0a20-109">Créé par:</span><span class="sxs-lookup"><span data-stu-id="f0a20-109">Created by:</span></span>  <br/> |<span data-ttu-id="f0a20-110">Fournisseur de magasin</span><span class="sxs-lookup"><span data-stu-id="f0a20-110">Store provider</span></span>  <br/> |
|<span data-ttu-id="f0a20-111">Accès par:</span><span class="sxs-lookup"><span data-stu-id="f0a20-111">Accessed by:</span></span>  <br/> |<span data-ttu-id="f0a20-112">Outlook et d'autres clients</span><span class="sxs-lookup"><span data-stu-id="f0a20-112">Outlook and other clients</span></span>  <br/> |
|<span data-ttu-id="f0a20-113">Type de propriété:</span><span class="sxs-lookup"><span data-stu-id="f0a20-113">Property type:</span></span>  <br/> |<span data-ttu-id="f0a20-114">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f0a20-114">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f0a20-115">Type d'accès:</span><span class="sxs-lookup"><span data-stu-id="f0a20-115">Access type:</span></span>  <br/> |<span data-ttu-id="f0a20-116">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="f0a20-116">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0a20-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="f0a20-117">Remarks</span></span>

<span data-ttu-id="f0a20-118">Pour fournir l'une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMAPIProp: IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour l'une des propriétés transmises à un appel [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a20-118">To provide any of the store functionality, the store provider must implement [IMAPIProp : IUnknown](imapipropiunknown.md) and return a valid property tag for any of these properties passed to an [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) call.</span></span> <span data-ttu-id="f0a20-119">Lorsque la balise de propriété de l'une de ces propriétés est transmise à [IMAPIProp:: GetProps](imapiprop-getprops.md), le fournisseur Store doit également renvoyer la valeur de propriété correcte.</span><span class="sxs-lookup"><span data-stu-id="f0a20-119">When the property tag for any of these properties is passed to [IMAPIProp::GetProps](imapiprop-getprops.md), the store provider must also return the correct property value.</span></span> <span data-ttu-id="f0a20-120">Les fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f0a20-120">Store providers can call [HrGetOneProp](hrgetoneprop.md) and [HrSetOneProp](hrsetoneprop.md) to get or set these properties.</span></span> 
  
<span data-ttu-id="f0a20-121">Pour récupérer la valeur de cette propriété, le client doit d'abord utiliser [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp:: GetProps](imapiprop-getprops.md) pour obtenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="f0a20-121">To retrieve the value of this property, the client should first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="f0a20-122">Lors de l'appel de [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d'entrée _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="f0a20-122">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f0a20-123">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="f0a20-123">lpGuid:</span></span>  <br/> |<span data-ttu-id="f0a20-124">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="f0a20-124">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="f0a20-125">ulKind:</span><span class="sxs-lookup"><span data-stu-id="f0a20-125">ulKind:</span></span>  <br/> |<span data-ttu-id="f0a20-126">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="f0a20-126">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="f0a20-127">Kind. lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="f0a20-127">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="f0a20-128">L "urn: schemas-microsoft-com: Office: Outlook # allornonemtgupdatedlg"</span><span class="sxs-lookup"><span data-stu-id="f0a20-128">L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"</span></span>  <br/> |
   
<span data-ttu-id="f0a20-129">Un fournisseur de banque qui utilise un serveur pour envoyer des mises à jour de réunion peut modifier la boîte **de dialogue Envoyer une mise à jour aux participants** .</span><span class="sxs-lookup"><span data-stu-id="f0a20-129">A store provider that uses a server to send meeting updates can modify the **Send Update to Attendees** dialog box.</span></span> <span data-ttu-id="f0a20-130">Cette fonctionnalité est utile car lorsque le serveur envoie une mise à jour de réunion, le serveur ne sait pas quels participants ont été ajoutés ou supprimés par l'utilisateur depuis la demande de réunion initiale.</span><span class="sxs-lookup"><span data-stu-id="f0a20-130">This functionality is useful because when the server sends a meeting update, the server does not know which attendees have been added or deleted by the user since the initial meeting request.</span></span> <span data-ttu-id="f0a20-131">Lorsque cette propriété a la **valeur true**, l'option **Envoyer la mise à jour uniquement vers les participants ajoutés ou supprimés** n'est pas affichée dans la boîte de dialogue **Envoyer la mise à jour aux participants** .</span><span class="sxs-lookup"><span data-stu-id="f0a20-131">When this property is **true**, the **Send update only to added or deleted attendees** option is not displayed in the **Send Update to Attendees** dialog box.</span></span> 
  
<span data-ttu-id="f0a20-132">Cette propriété est ignorée si la version d'Outlook est antérieure à Microsoft Office Outlook 2003 Service Pack 1, ou si sa valeur \*\*\*\* est false.</span><span class="sxs-lookup"><span data-stu-id="f0a20-132">This property is ignored if the version of Outlook is earlier than Microsoft Office Outlook 2003 Service Pack 1, or if its value is **false**.</span></span>
  

