---
title: Propriété canonique PidTagAddressBookChooseDirectoryAutomatically
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b685fd0ebe4a2d0bfcfd8aab3015602b84932db7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564940"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a><span data-ttu-id="047b5-103">Propriété canonique PidTagAddressBookChooseDirectoryAutomatically</span><span class="sxs-lookup"><span data-stu-id="047b5-103">PidTagAddressBookChooseDirectoryAutomatically Canonical Property</span></span>

  
  
<span data-ttu-id="047b5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="047b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="047b5-105">Permet à Microsoft Outlook 2010 et Microsoft Outlook 2013 de choisir la liste d’adresses globale (GAL) plus appropriée ou le dossier de contacts pour la boîte aux lettres en cours.</span><span class="sxs-lookup"><span data-stu-id="047b5-105">Enables Microsoft Outlook 2010 and Microsoft Outlook 2013 to choose the most appropriate global address list (GAL) or contact folder for the current mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="047b5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="047b5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="047b5-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="047b5-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span></span>  <br/> |
|<span data-ttu-id="047b5-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="047b5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="047b5-109">0x3D1C000B</span><span class="sxs-lookup"><span data-stu-id="047b5-109">0x3D1C000B</span></span>  <br/> |
|<span data-ttu-id="047b5-110">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="047b5-110">Property type:</span></span>  <br/> |<span data-ttu-id="047b5-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="047b5-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="047b5-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="047b5-112">Area:</span></span>  <br/> |<span data-ttu-id="047b5-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="047b5-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="047b5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="047b5-114">Remarks</span></span>

<span data-ttu-id="047b5-115">Cette propriété correspond au paramètre **d’Accepter automatiquement** dans la boîte de dialogue Options de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="047b5-115">This property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="047b5-116">Lorsque cette propriété existe dans la section profil IID_CAPONE_PROF et est définie sur **true**, le carnet d’adresses, boîte de dialogue par défaut, le conteneur spécifié par la méthode [SetDefaultDir](iaddrbook-setdefaultdir.md) n’est plus mais choisit un carnet d’adresses qui Outlook 2010 ou Outlook 2013 estime appropriée pour le contexte dans lequel la boîte de dialogue a été affiché.</span><span class="sxs-lookup"><span data-stu-id="047b5-116">When this property exists in the IID_CAPONE_PROF profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by the [SetDefaultDir](iaddrbook-setdefaultdir.md) method, but chooses an address book that Outlook 2010 or Outlook 2013 considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="047b5-117">Notez que cela peut entraîner une mauvaise expérience pour les fournisseurs de carnet d’adresses tiers.</span><span class="sxs-lookup"><span data-stu-id="047b5-117">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="047b5-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="047b5-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="047b5-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="047b5-119">Header files</span></span>

<span data-ttu-id="047b5-120">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="047b5-120">Mapitags.h</span></span>
  
> <span data-ttu-id="047b5-121">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="047b5-121">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="047b5-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="047b5-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="047b5-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="047b5-123">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="047b5-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="047b5-124">See also</span></span>



[<span data-ttu-id="047b5-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="047b5-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="047b5-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="047b5-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="047b5-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="047b5-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="047b5-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="047b5-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="047b5-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="047b5-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

