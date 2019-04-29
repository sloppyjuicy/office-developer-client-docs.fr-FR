---
title: Affichage des informations du destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e1c31e5edf702dd8f172f67e7055a96ae4cfff1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412953"
---
# <a name="displaying-recipient-information"></a><span data-ttu-id="4f7a2-103">Affichage des informations du destinataire</span><span class="sxs-lookup"><span data-stu-id="4f7a2-103">Displaying recipient information</span></span>

<span data-ttu-id="4f7a2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f7a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f7a2-105">MAPI fournit une boîte de dialogue commune pour afficher les détails des destinataires.</span><span class="sxs-lookup"><span data-stu-id="4f7a2-105">MAPI provides a common dialog box for showing recipient details.</span></span> <span data-ttu-id="4f7a2-106">La boîte de dialogue détails est créée à partir d'une table d'affichage et d'une implémentation **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="4f7a2-106">The details dialog box is created from a display table and an **IMAPIProp** implementation.</span></span> <span data-ttu-id="4f7a2-107">Le tableau d'affichage décrit l'apparence de l'affichage des détails et l'implémentation **IMAPIProp** contrôle les données du destinataire.</span><span class="sxs-lookup"><span data-stu-id="4f7a2-107">The display table describes the appearance of the details display and the **IMAPIProp** implementation controls the data for the recipient.</span></span> <span data-ttu-id="4f7a2-108">Votre fournisseur est responsable de la fourniture de la table d'affichage et de l'implémentation **IMAPIProp** pour chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="4f7a2-108">Your provider is responsible for supplying the display table and the **IMAPIProp** implementation for each recipient.</span></span> 
  
<span data-ttu-id="4f7a2-109">Le moyen le plus simple de créer la table d'affichage consiste à définir une structure [DTPAGE](dtpage.md) et à appeler [BuildDisplayTable](builddisplaytable.md).</span><span class="sxs-lookup"><span data-stu-id="4f7a2-109">The easiest way to create the display table is to define a [DTPAGE](dtpage.md) structure and call [BuildDisplayTable](builddisplaytable.md).</span></span> <span data-ttu-id="4f7a2-110">Toutefois, certains fournisseurs, en particulier des fournisseurs en lecture seule qui permettent la création de destinataires uniques, utilisent **IPropData**.</span><span class="sxs-lookup"><span data-stu-id="4f7a2-110">However, some providers, specifically read-only providers that allow the creation of one-off recipients, use **IPropData**.</span></span> <span data-ttu-id="4f7a2-111">L'implémentation de **IMAPIProp** peut être n'importe quel type d'objet Property.</span><span class="sxs-lookup"><span data-stu-id="4f7a2-111">The **IMAPIProp** implementation can be any type of property object.</span></span> 
  
<span data-ttu-id="4f7a2-112">Il existe deux méthodes pour appeler cette boîte de dialogue: [IAddrBook::D etails](iaddrbook-details.md) et [IMAPISupport::D etails](imapisupport-details.md).</span><span class="sxs-lookup"><span data-stu-id="4f7a2-112">There are two methods for invoking this dialog box: [IAddrBook::Details](iaddrbook-details.md) and [IMAPISupport::Details](imapisupport-details.md).</span></span> <span data-ttu-id="4f7a2-113">Lorsque votre fournisseur appelle l'une de ces méthodes pour demander les détails d'un destinataire, MAPI ouvre d'abord le destinataire en appelant la méthode [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) de son conteneur.</span><span class="sxs-lookup"><span data-stu-id="4f7a2-113">When your provider calls one of these methods to request details for a recipient, MAPI first opens the recipient by calling its container's [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method.</span></span> <span data-ttu-id="4f7a2-114">Il appelle ensuite la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) du destinataire pour demander la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4f7a2-114">Next it calls the recipient's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to request the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="4f7a2-115">**PR_DETAILS_TABLE** est la propriété qui représente la table d'affichage des détails d'un destinataire.</span><span class="sxs-lookup"><span data-stu-id="4f7a2-115">**PR_DETAILS_TABLE** is the property that represents a recipient's details display table.</span></span> 
  
<span data-ttu-id="4f7a2-116">L'interface [IPropData: IMAPIProp](ipropdataimapiprop.md) peut être utilisée pour surveiller les modifications apportées aux contrôles d'affichage de table, comme décrit dans la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="4f7a2-116">The [IPropData : IMAPIProp](ipropdataimapiprop.md) interface can be used to monitor changes on display table controls as described in the following procedure.</span></span> 
  
## <a name="monitor-changes-to-a-control"></a><span data-ttu-id="4f7a2-117">Surveiller les modifications apportées à un contrôle</span><span class="sxs-lookup"><span data-stu-id="4f7a2-117">Monitor changes to a control</span></span>
  
1. <span data-ttu-id="4f7a2-118">Avant que l'utilisateur n'accède au contrôle, appelez [IPropData:: HrSetObjAccess](ipropdata-hrsetobjaccess.md) pour définir l'accès du contrôle à IPROP_CLEAN.</span><span class="sxs-lookup"><span data-stu-id="4f7a2-118">Before the user gains access to the control, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) to set the control's access to IPROP_CLEAN.</span></span> 
    
2. <span data-ttu-id="4f7a2-119">Autoriser l'utilisateur à travailler avec la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="4f7a2-119">Allow the user to work with the dialog box.</span></span> 
    
3. <span data-ttu-id="4f7a2-120">Lorsque l'utilisateur a terminé, appelez [IPropData:: HrGetPropAccess](ipropdata-hrgetpropaccess.md) pour récupérer le niveau d'accès actuel du contrôle.</span><span class="sxs-lookup"><span data-stu-id="4f7a2-120">When the user has finished, call [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) to retrieve the current access level of the control.</span></span> 
    
4. <span data-ttu-id="4f7a2-121">Si le niveau d'accès est IPROP_DIRTY, l'utilisateur a modifié le contrôle.</span><span class="sxs-lookup"><span data-stu-id="4f7a2-121">If the access level is IPROP_DIRTY, the user has modified the control.</span></span> <span data-ttu-id="4f7a2-122">Votre fournisseur doit:</span><span class="sxs-lookup"><span data-stu-id="4f7a2-122">Your provider should:</span></span>
    
   - <span data-ttu-id="4f7a2-123">Appelez [IPropData:: HrSetPropAccess](ipropdata-hrsetpropaccess.md) pour redéfinir le niveau d'accès sur IPROP_CLEAN.</span><span class="sxs-lookup"><span data-stu-id="4f7a2-123">Call [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) to set the access level back to IPROP_CLEAN.</span></span> 
    
   - <span data-ttu-id="4f7a2-124">Appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de l'objet de données de propriété pour extraire la propriété modifiée et la mettre à jour en appelant [IMAPIProp:: SetProps](imapiprop-setprops.md).</span><span class="sxs-lookup"><span data-stu-id="4f7a2-124">Call the property data object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the changed property and update it by calling [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span>
    
5. <span data-ttu-id="4f7a2-125">Si le niveau d'accès est toujours IPROP_CLEAN, le contrôle n'a pas été modifié.</span><span class="sxs-lookup"><span data-stu-id="4f7a2-125">If the access level is still IPROP_CLEAN, the control has not been modified.</span></span> 
    
<span data-ttu-id="4f7a2-126">Pour plus d'informations sur la création de tables d'affichage, voir [afficher les tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="4f7a2-126">For more information about creating display tables, see [Display Tables](display-tables.md).</span></span>
  

