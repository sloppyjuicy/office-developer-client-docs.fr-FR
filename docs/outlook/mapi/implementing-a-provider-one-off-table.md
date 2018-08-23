---
title: Implémentation d’une table ponctuelle de fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f484174bd0a83c9bb874bec4896fe3dd925405c7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568237"
---
# <a name="implementing-a-provider-one-off-table"></a><span data-ttu-id="11caa-103">Implémentation d’une table ponctuelle de fournisseur</span><span class="sxs-lookup"><span data-stu-id="11caa-103">Implementing a Provider One-Off Table</span></span>

  
  
<span data-ttu-id="11caa-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11caa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11caa-105">MAPI appelle la méthode [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) de votre fournisseur lorsque l’utilisateur d’une application cliente ajoute un destinataire à un message sortant.</span><span class="sxs-lookup"><span data-stu-id="11caa-105">MAPI calls your provider's [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method when the user of a client application adds a recipient to an outgoing message.</span></span> <span data-ttu-id="11caa-106">En règle générale, les types d’adresses demandés sont spécifiques à votre système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="11caa-106">Typically, the types of addresses requested are unique to your messaging system.</span></span> <span data-ttu-id="11caa-107">Si votre fournisseur prend en charge la création de destinataires, elle doit fournir une table unique qui expose des modèles pour chaque type d’adresse du destinataire pris en charge.</span><span class="sxs-lookup"><span data-stu-id="11caa-107">If your provider supports recipient creation, it must supply a one-off table that exposes templates for every type of supported recipient address.</span></span> <span data-ttu-id="11caa-108">Si votre fournisseur ne gère pas la création de destinataires, renvoyer MAPI_E_NO_SUPPORT à partir de l’appel **GetOneOffTable** .</span><span class="sxs-lookup"><span data-stu-id="11caa-108">If your provider does not support recipient creation, return MAPI_E_NO_SUPPORT from the **GetOneOffTable** call.</span></span> 
  
<span data-ttu-id="11caa-109">MAPI généralement conserve table uniques de votre fournisseur ouvert pour la durée de vie de la session, libérer uniquement lorsqu’un client appelle soit du sous-système ou méthode de [IMAPIStatus::ValidateState](imapistatus-validatestate.md) du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="11caa-109">MAPI will typically keep your provider's one-off table open for the lifetime of the session, releasing it only when a client calls either the subsystem's or address book's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="11caa-110">MAPI inscrit pour les notifications sur ce tableau afin que si les modèles sont ajoutées ou supprimées, ces modifications peuvent être reflétées à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="11caa-110">MAPI registers for notifications on this table so that if templates are added or deleted, these changes can be reflected to the user.</span></span> 
  
 <span data-ttu-id="11caa-111">**Pour mettre en œuvre IABLogon::GetOneOffTable**</span><span class="sxs-lookup"><span data-stu-id="11caa-111">**To implement IABLogon::GetOneOffTable**</span></span>
  
1. <span data-ttu-id="11caa-112">Vérifiez la valeur du paramètre flags, _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="11caa-112">Check the value of the flags parameter,  _ulFlags_.</span></span> <span data-ttu-id="11caa-113">Si l’indicateur MAPI_UNICODE est défini et que votre fournisseur ne prend pas en charge Unicode, échouer et retourner MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="11caa-113">If the MAPI_UNICODE flag is set and your provider does not support Unicode, fail and return MAPI_E_BAD_CHARWIDTH.</span></span> 
    
2. <span data-ttu-id="11caa-114">Vérifiez si uniques table votre fournisseur a déjà été créée.</span><span class="sxs-lookup"><span data-stu-id="11caa-114">Check if your provider's one-off table has already been created.</span></span> <span data-ttu-id="11caa-115">Étant donné que les tables uniques sont généralement statiques, votre fournisseur n’a jamais transitent par le processus de création de plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="11caa-115">Because one-off tables are typically static, your provider never has to go through the creation process more than once.</span></span> <span data-ttu-id="11caa-116">Si une table existe déjà, retourne un pointeur à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="11caa-116">If a table already exists, return a pointer to it.</span></span> 
    
3. <span data-ttu-id="11caa-117">Si une table unique n’existe pas, appelez **Create table** pour en créer une.</span><span class="sxs-lookup"><span data-stu-id="11caa-117">If a one-off table does not yet exist, call **CreateTable** to create one.</span></span> 
    
4. <span data-ttu-id="11caa-118">Définissez les propriétés suivantes pour les colonnes dans les lignes de la table :</span><span class="sxs-lookup"><span data-stu-id="11caa-118">Set the following properties for the columns in your table rows:</span></span>
    
  - <span data-ttu-id="11caa-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) sur le nom du type de destinataire que le modèle peut créer.</span><span class="sxs-lookup"><span data-stu-id="11caa-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to the name of the type of recipient that the template can create.</span></span> 
    
  - <span data-ttu-id="11caa-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à l’identificateur d’entrée pour le modèle unique.</span><span class="sxs-lookup"><span data-stu-id="11caa-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) to the entry identifier for the one-off template.</span></span>
    
  - <span data-ttu-id="11caa-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) pour indiquer le niveau de hiérarchie dans l’affichage tableau uniques.</span><span class="sxs-lookup"><span data-stu-id="11caa-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) to indicate the hierarchy level in the one-off table display.</span></span>
    
  - <span data-ttu-id="11caa-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) la valeur True pour indiquer si la ligne représente un modèle et la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="11caa-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) to TRUE to indicate if the row represents a template and FALSE otherwise.</span></span>
    
  - <span data-ttu-id="11caa-123">**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) pour le type d’adresse créé par le modèle.</span><span class="sxs-lookup"><span data-stu-id="11caa-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the type of address created by the template.</span></span>
    
  - <span data-ttu-id="11caa-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) DT_MAILUSER ou une autre valeur qui indique le type d’affichage pour le modèle.</span><span class="sxs-lookup"><span data-stu-id="11caa-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or another value that indicates the type of display for the template.</span></span>
    
  - <span data-ttu-id="11caa-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) une valeur binaire unique.</span><span class="sxs-lookup"><span data-stu-id="11caa-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) to a unique binary value.</span></span> 
    
5. <span data-ttu-id="11caa-126">Appelez [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) pour modifier la table directement.</span><span class="sxs-lookup"><span data-stu-id="11caa-126">Call [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) to modify the table directly.</span></span> 
    
6. <span data-ttu-id="11caa-127">Appelez [ITableData::HrGetView](itabledata-hrgetview.md) pour créer une implémentation d’interface **IMAPITable** pour revenir à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="11caa-127">Call [ITableData::HrGetView](itabledata-hrgetview.md) to create an **IMAPITable** interface implementation to return to the caller.</span></span> 
    

