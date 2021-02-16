---
title: Mise en œuvre d’une table One-Off fournisseur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 023686702b76b5b29acf4304fcfdb3377e8cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436292"
---
# <a name="implementing-a-provider-one-off-table"></a><span data-ttu-id="f965a-103">Mise en œuvre d’une table One-Off fournisseur</span><span class="sxs-lookup"><span data-stu-id="f965a-103">Implementing a Provider One-Off Table</span></span>

  
  
<span data-ttu-id="f965a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f965a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f965a-105">MAPI appelle la méthode [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) de votre fournisseur lorsque l’utilisateur d’une application cliente ajoute un destinataire à un message sortant.</span><span class="sxs-lookup"><span data-stu-id="f965a-105">MAPI calls your provider's [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method when the user of a client application adds a recipient to an outgoing message.</span></span> <span data-ttu-id="f965a-106">En règle générale, les types d’adresses demandés sont propres à votre système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="f965a-106">Typically, the types of addresses requested are unique to your messaging system.</span></span> <span data-ttu-id="f965a-107">Si votre fournisseur prend en charge la création de destinataires, il doit fournir un tableau unique qui expose des modèles pour chaque type d’adresse de destinataire prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f965a-107">If your provider supports recipient creation, it must supply a one-off table that exposes templates for every type of supported recipient address.</span></span> <span data-ttu-id="f965a-108">Si votre fournisseur ne prend pas en charge la création de destinataires, MAPI_E_NO_SUPPORT à partir de **l’appel GetOneOffTable.**</span><span class="sxs-lookup"><span data-stu-id="f965a-108">If your provider does not support recipient creation, return MAPI_E_NO_SUPPORT from the **GetOneOffTable** call.</span></span> 
  
<span data-ttu-id="f965a-109">MAPI conserve généralement la table unique de votre fournisseur ouverte pendant toute la durée de vie de la session, en la libérant uniquement lorsqu’un client appelle la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) du sous-système ou du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="f965a-109">MAPI will typically keep your provider's one-off table open for the lifetime of the session, releasing it only when a client calls either the subsystem's or address book's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="f965a-110">MAPI s’inscrit pour les notifications dans ce tableau afin que si des modèles sont ajoutés ou supprimés, ces modifications peuvent être reflétées pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f965a-110">MAPI registers for notifications on this table so that if templates are added or deleted, these changes can be reflected to the user.</span></span> 
  
 <span data-ttu-id="f965a-111">**Pour implémenter IABLogon::GetOneOffTable**</span><span class="sxs-lookup"><span data-stu-id="f965a-111">**To implement IABLogon::GetOneOffTable**</span></span>
  
1. <span data-ttu-id="f965a-112">Vérifiez la valeur du paramètre d’indicateurs,  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="f965a-112">Check the value of the flags parameter,  _ulFlags_.</span></span> <span data-ttu-id="f965a-113">Si l’MAPI_UNICODE est définie et que votre fournisseur ne prend pas en charge Unicode, échouez et renvoyez MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="f965a-113">If the MAPI_UNICODE flag is set and your provider does not support Unicode, fail and return MAPI_E_BAD_CHARWIDTH.</span></span> 
    
2. <span data-ttu-id="f965a-114">Vérifiez si la table one-off de votre fournisseur a déjà été créée.</span><span class="sxs-lookup"><span data-stu-id="f965a-114">Check if your provider's one-off table has already been created.</span></span> <span data-ttu-id="f965a-115">Étant donné que les tables unique sont généralement statiques, votre fournisseur n’a jamais à passer par le processus de création plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="f965a-115">Because one-off tables are typically static, your provider never has to go through the creation process more than once.</span></span> <span data-ttu-id="f965a-116">Si un tableau existe déjà, renvoyer un pointeur vers ce tableau.</span><span class="sxs-lookup"><span data-stu-id="f965a-116">If a table already exists, return a pointer to it.</span></span> 
    
3. <span data-ttu-id="f965a-117">Si une table non existante n’existe pas encore, appelez **CreateTable** pour en créer une.</span><span class="sxs-lookup"><span data-stu-id="f965a-117">If a one-off table does not yet exist, call **CreateTable** to create one.</span></span> 
    
4. <span data-ttu-id="f965a-118">Définissez les propriétés suivantes pour les colonnes dans les lignes de votre tableau :</span><span class="sxs-lookup"><span data-stu-id="f965a-118">Set the following properties for the columns in your table rows:</span></span>
    
  - <span data-ttu-id="f965a-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) au nom du type de destinataire que le modèle peut créer.</span><span class="sxs-lookup"><span data-stu-id="f965a-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to the name of the type of recipient that the template can create.</span></span> 
    
  - <span data-ttu-id="f965a-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à l’identificateur d’entrée pour le modèle unique.</span><span class="sxs-lookup"><span data-stu-id="f965a-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) to the entry identifier for the one-off template.</span></span>
    
  - <span data-ttu-id="f965a-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) pour indiquer le niveau de hiérarchie dans l’affichage du tableau.</span><span class="sxs-lookup"><span data-stu-id="f965a-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) to indicate the hierarchy level in the one-off table display.</span></span>
    
  - <span data-ttu-id="f965a-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) à TRUE pour indiquer si la ligne représente un modèle et FALSE dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f965a-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) to TRUE to indicate if the row represents a template and FALSE otherwise.</span></span>
    
  - <span data-ttu-id="f965a-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) au type d’adresse créé par le modèle.</span><span class="sxs-lookup"><span data-stu-id="f965a-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the type of address created by the template.</span></span>
    
  - <span data-ttu-id="f965a-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) pour DT_MAILUSER ou une autre valeur qui indique le type d’affichage pour le modèle.</span><span class="sxs-lookup"><span data-stu-id="f965a-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or another value that indicates the type of display for the template.</span></span>
    
  - <span data-ttu-id="f965a-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) à une valeur binaire unique.</span><span class="sxs-lookup"><span data-stu-id="f965a-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) to a unique binary value.</span></span> 
    
5. <span data-ttu-id="f965a-126">Appelez [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) pour modifier directement la table.</span><span class="sxs-lookup"><span data-stu-id="f965a-126">Call [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) to modify the table directly.</span></span> 
    
6. <span data-ttu-id="f965a-127">Appelez [ITableData::HrGetView](itabledata-hrgetview.md) pour créer une implémentation d’interface **IMAPITable** pour revenir à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="f965a-127">Call [ITableData::HrGetView](itabledata-hrgetview.md) to create an **IMAPITable** interface implementation to return to the caller.</span></span> 
    

