---
title: Propriétés de destinataire pour tous les Messages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18c96796-f38d-4058-9c51-9c5a14990846
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d92e9dbbf594dffc3dbf5bbf271fc80a0abed68e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786964"
---
# <a name="recipient-properties-for-all-messages"></a><span data-ttu-id="a89a5-103">Propriétés de destinataire pour tous les Messages</span><span class="sxs-lookup"><span data-stu-id="a89a5-103">Recipient Properties for All Messages</span></span>

  
  
<span data-ttu-id="a89a5-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a89a5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a89a5-105">Les propriétés suivantes sont généralement présentes à tous les destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="a89a5-105">The following properties are typically present for all message recipients.</span></span> <span data-ttu-id="a89a5-106">**ADRESSE_EMAIL_PR** et **clé PR_SEARCH_KEY** sont facultatives ; toutes les autres propriétés sont requis.</span><span class="sxs-lookup"><span data-stu-id="a89a5-106">**PR_EMAIL_ADDRESS** and **PR_SEARCH_KEY** are optional; all of the other properties are required.</span></span> 
  
<span data-ttu-id="a89a5-107">**Titre de la table**</span><span class="sxs-lookup"><span data-stu-id="a89a5-107">**Table Title**</span></span>

|<span data-ttu-id="a89a5-108">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="a89a5-108">**Property**</span></span>|<span data-ttu-id="a89a5-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="a89a5-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a89a5-110">**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a89a5-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a89a5-111">Contient le type d’adresse de messagerie de l’utilisateur de messagerie, tels que SMTP.</span><span class="sxs-lookup"><span data-stu-id="a89a5-111">Contains the messaging user's email address type, such as SMTP.</span></span>  <br/> |
|<span data-ttu-id="a89a5-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a89a5-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a89a5-113">Contient le nom complet d’un objet MAPI donné.</span><span class="sxs-lookup"><span data-stu-id="a89a5-113">Contains the display name for a given MAPI object.</span></span>  <br/> |
|<span data-ttu-id="a89a5-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a89a5-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a89a5-115">Contient une valeur utilisée pour associer une icône à une ligne particulière d’une table.</span><span class="sxs-lookup"><span data-stu-id="a89a5-115">Contains a value used to associate an icon with a particular row of a table.</span></span>  <br/> |
|<span data-ttu-id="a89a5-116">**ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a89a5-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a89a5-117">Contient l’adresse de messagerie de l’utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="a89a5-117">Contains the messaging user's email address.</span></span>  <br/> |
|<span data-ttu-id="a89a5-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a89a5-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a89a5-119">Contient un identificateur d’entrée MAPI utilisé pour ouvrir et modifier les propriétés d’un objet MAPI particulier.</span><span class="sxs-lookup"><span data-stu-id="a89a5-119">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span>  <br/> |
|<span data-ttu-id="a89a5-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a89a5-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a89a5-121">Contient le type d’un objet.</span><span class="sxs-lookup"><span data-stu-id="a89a5-121">Contains the type of an object.</span></span>  <br/> |
|<span data-ttu-id="a89a5-122">**Clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a89a5-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a89a5-123">Contient une clé comparable binaire qui identifie les objets en corrélation pour une recherche.</span><span class="sxs-lookup"><span data-stu-id="a89a5-123">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>  <br/> |
   

