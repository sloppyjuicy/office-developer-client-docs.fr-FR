---
title: Affichage des informations sur les destinataires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4610d9e643541e39144f2af86a2d64928b8e9ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591288"
---
# <a name="displaying-recipient-information"></a><span data-ttu-id="8478a-103">Affichage des informations sur les destinataires</span><span class="sxs-lookup"><span data-stu-id="8478a-103">Displaying recipient information</span></span>

<span data-ttu-id="8478a-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8478a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8478a-105">MAPI fournit une boîte de dialogue pour afficher des détails sur le destinataires.</span><span class="sxs-lookup"><span data-stu-id="8478a-105">MAPI provides a common dialog box for showing recipient details.</span></span> <span data-ttu-id="8478a-106">La boîte de dialogue Détails est créée à partir d’un tableau d’affichage et une implémentation **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="8478a-106">The details dialog box is created from a display table and an **IMAPIProp** implementation.</span></span> <span data-ttu-id="8478a-107">Le tableau de l’affichage décrit l’apparence de l’affichage des détails et l’implémentation **IMAPIProp** contrôle les données pour le destinataire.</span><span class="sxs-lookup"><span data-stu-id="8478a-107">The display table describes the appearance of the details display and the **IMAPIProp** implementation controls the data for the recipient.</span></span> <span data-ttu-id="8478a-108">Votre fournisseur est chargé de fournir le tableau d’affichage et l’implémentation **IMAPIProp** pour chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="8478a-108">Your provider is responsible for supplying the display table and the **IMAPIProp** implementation for each recipient.</span></span> 
  
<span data-ttu-id="8478a-109">Pour créer la table d’affichage le plus simple consiste à définir une structure [DTPAGE](dtpage.md) et appelez [BuildDisplayTable](builddisplaytable.md).</span><span class="sxs-lookup"><span data-stu-id="8478a-109">The easiest way to create the display table is to define a [DTPAGE](dtpage.md) structure and call [BuildDisplayTable](builddisplaytable.md).</span></span> <span data-ttu-id="8478a-110">Toutefois, certains fournisseurs, spécifiquement fournisseurs en lecture seule qui permettent la création de destinataires uniques, utilisent **IPropData**.</span><span class="sxs-lookup"><span data-stu-id="8478a-110">However, some providers, specifically read-only providers that allow the creation of one-off recipients, use **IPropData**.</span></span> <span data-ttu-id="8478a-111">L’implémentation **IMAPIProp** peut être n’importe quel type d’objet property.</span><span class="sxs-lookup"><span data-stu-id="8478a-111">The **IMAPIProp** implementation can be any type of property object.</span></span> 
  
<span data-ttu-id="8478a-112">Il existe deux méthodes pour l’appel de cette boîte de dialogue : [IAddrBook::Details](iaddrbook-details.md) et [IMAPISupport::Details](imapisupport-details.md).</span><span class="sxs-lookup"><span data-stu-id="8478a-112">There are two methods for invoking this dialog box: [IAddrBook::Details](iaddrbook-details.md) and [IMAPISupport::Details](imapisupport-details.md).</span></span> <span data-ttu-id="8478a-113">Lorsque votre fournisseur appelle une de ces méthodes pour demander les détails pour un destinataire, MAPI commence par le destinataire en appelant la méthode de [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) de son conteneur.</span><span class="sxs-lookup"><span data-stu-id="8478a-113">When your provider calls one of these methods to request details for a recipient, MAPI first opens the recipient by calling its container's [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method.</span></span> <span data-ttu-id="8478a-114">Il appelle ensuite la méthode de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du destinataire pour demander la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8478a-114">Next it calls the recipient's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to request the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="8478a-115">**PR_DETAILS_TABLE** est la propriété qui représente la table affichage de détails d’un destinataire.</span><span class="sxs-lookup"><span data-stu-id="8478a-115">**PR_DETAILS_TABLE** is the property that represents a recipient's details display table.</span></span> 
  
<span data-ttu-id="8478a-116">La [IPropData : IMAPIProp](ipropdataimapiprop.md) interface peut être utilisée pour surveiller les modifications sur les contrôles d’affichage de tableau comme décrit dans la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="8478a-116">The [IPropData : IMAPIProp](ipropdataimapiprop.md) interface can be used to monitor changes on display table controls as described in the following procedure.</span></span> 
  
## <a name="monitor-changes-to-a-control"></a><span data-ttu-id="8478a-117">Surveiller les modifications à un contrôle</span><span class="sxs-lookup"><span data-stu-id="8478a-117">Monitor changes to a control</span></span>
  
1. <span data-ttu-id="8478a-118">Avant que l’utilisateur accède au contrôle, appelez [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) pour définir l’accès au contrôle IPROP_CLEAN.</span><span class="sxs-lookup"><span data-stu-id="8478a-118">Before the user gains access to the control, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) to set the control's access to IPROP_CLEAN.</span></span> 
    
2. <span data-ttu-id="8478a-119">Autoriser l’utilisateur à l’utilisation de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8478a-119">Allow the user to work with the dialog box.</span></span> 
    
3. <span data-ttu-id="8478a-120">Lorsque l’utilisateur a terminé, appelez [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) pour récupérer le niveau d’accès actuel du contrôle.</span><span class="sxs-lookup"><span data-stu-id="8478a-120">When the user has finished, call [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) to retrieve the current access level of the control.</span></span> 
    
4. <span data-ttu-id="8478a-121">Si le niveau d’accès est IPROP_DIRTY, l’utilisateur a modifié le contrôle.</span><span class="sxs-lookup"><span data-stu-id="8478a-121">If the access level is IPROP_DIRTY, the user has modified the control.</span></span> <span data-ttu-id="8478a-122">Votre fournisseur doit :</span><span class="sxs-lookup"><span data-stu-id="8478a-122">Your provider should:</span></span>
    
   - <span data-ttu-id="8478a-123">Appelez [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) pour définir l’accès au niveau au IPROP_CLEAN.</span><span class="sxs-lookup"><span data-stu-id="8478a-123">Call [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) to set the access level back to IPROP_CLEAN.</span></span> 
    
   - <span data-ttu-id="8478a-124">Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’objet de données de propriété pour récupérer la propriété modifiée et le mettre à jour en appelant [IMAPIProp::SetProps](imapiprop-setprops.md).</span><span class="sxs-lookup"><span data-stu-id="8478a-124">Call the property data object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the changed property and update it by calling [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span>
    
5. <span data-ttu-id="8478a-125">Si le niveau d’accès est toujours IPROP_CLEAN, le contrôle n’a pas été modifié.</span><span class="sxs-lookup"><span data-stu-id="8478a-125">If the access level is still IPROP_CLEAN, the control has not been modified.</span></span> 
    
<span data-ttu-id="8478a-126">Pour plus d’informations sur la création de tableaux d’affichage, voir [Afficher les Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8478a-126">For more information about creating display tables, see [Display Tables](display-tables.md).</span></span>
  

