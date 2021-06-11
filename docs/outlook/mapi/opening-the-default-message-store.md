---
title: Ouverture de la banque de messages par défaut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d8e620516e2b3e61cd07f3a08af989cc4ed5b61e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436026"
---
# <a name="opening-the-default-message-store"></a><span data-ttu-id="84111-103">Ouverture de la banque de messages par défaut</span><span class="sxs-lookup"><span data-stu-id="84111-103">Opening the default message store</span></span>

<span data-ttu-id="84111-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84111-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84111-105">Dans une session particulière, une seule magasin de messages fait office de magasin de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="84111-105">In any particular session, one message store acts as the default message store.</span></span> <span data-ttu-id="84111-106">Une magasin de messages par défaut présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="84111-106">A default message store has the following characteristics:</span></span>
  
- <span data-ttu-id="84111-107">La **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) est définie sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="84111-107">The **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property is set to TRUE.</span></span>
    
- <span data-ttu-id="84111-108">L STATUS_DEFAULT_STORE est définie dans la **propriété PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="84111-108">The STATUS_DEFAULT_STORE flag is set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="84111-109">MAPI crée automatiquement la sous-arbre IPM et les dossiers racine pour les résultats de recherche, les affichages communs et les affichages personnels lorsque la magasin de messages est ouverte.</span><span class="sxs-lookup"><span data-stu-id="84111-109">MAPI automatically creates the IPM subtree and the root folders for search-results, common views and personal views when the message store is opened.</span></span> <span data-ttu-id="84111-110">Pour plus d’informations sur ces dossiers, voir [Sous-arbre IPM](ipm-subtree.md) et [Dossiers spéciaux MAPI.](mapi-special-folders.md)</span><span class="sxs-lookup"><span data-stu-id="84111-110">For more information about these folders, see [IPM Subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md).</span></span> 
    
<span data-ttu-id="84111-111">Pour récupérer l’identificateur d’entrée de la magasin de messages par défaut, vous devez appeler [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) pour ouvrir la table de la boutique de messages et appliquer une restriction appropriée dans un appel à [HrQueryAllRows](hrqueryallrows.md).</span><span class="sxs-lookup"><span data-stu-id="84111-111">To retrieve the entry identifier for the default message store, you must call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table and apply an appropriate restriction in a call to [HrQueryAllRows](hrqueryallrows.md).</span></span> <span data-ttu-id="84111-112">**HrQueryAllRows** retourne un ensemble de lignes avec la seule ligne qui représente la magasin de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="84111-112">**HrQueryAllRows** will return a row set with the one row that represents the default message store.</span></span> <span data-ttu-id="84111-113">La restriction que vous passez à **HrQueryAllRows** peut prendre l’une des formes suivantes :</span><span class="sxs-lookup"><span data-stu-id="84111-113">The restriction that you pass to **HrQueryAllRows** can take on one of the following forms:</span></span> 
  
1. <span data-ttu-id="84111-114">Restriction **AND** qui utilise une structure **SAndRestriction** pour combiner :</span><span class="sxs-lookup"><span data-stu-id="84111-114">An **AND** restriction that uses an **SAndRestriction** structure to combine:</span></span> 
    
   - <span data-ttu-id="84111-115">Il existe une restriction qui utilise une structure **SExistRestriction** pour tester l’existence de **la propriété PR_DEFAULT_STORE.**</span><span class="sxs-lookup"><span data-stu-id="84111-115">An exists restriction that uses an **SExistRestriction** structure to test for the existence of the **PR_DEFAULT_STORE** property.</span></span> 
    
   - <span data-ttu-id="84111-116">Restriction de propriété qui utilise une structure [SPropertyRestriction](spropertyrestriction.md) pour vérifier la valeur TRUE dans la **propriété PR_DEFAULT_STORE.**</span><span class="sxs-lookup"><span data-stu-id="84111-116">A property restriction that uses an [SPropertyRestriction](spropertyrestriction.md) structure to check for the TRUE value in the **PR_DEFAULT_STORE** property.</span></span> 
    
2. <span data-ttu-id="84111-117">Restriction de masque de bits qui utilise une structure [SBitMaskRestriction](sbitmaskrestriction.md) pour appliquer des STATUS_DEFAULT_STORE en tant que masque à la **propriété PR_RESOURCE_FLAGS.**</span><span class="sxs-lookup"><span data-stu-id="84111-117">A bitmask restriction that uses an [SBitMaskRestriction](sbitmaskrestriction.md) structure for applying STATUS_DEFAULT_STORE as a mask against the **PR_RESOURCE_FLAGS** property.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="84111-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84111-118">See also</span></span>

- [<span data-ttu-id="84111-119">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="84111-119">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="84111-120">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="84111-120">SAndRestriction</span></span>](sandrestriction.md)

