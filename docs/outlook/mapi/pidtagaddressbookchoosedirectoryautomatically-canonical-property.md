---
title: Propriété canonique PidTagAddressBookChooseDirectoryAutomatically
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 48dfced07a8fd78a1af22679759effbd3c6da343
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785679"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a><span data-ttu-id="5621d-103">Propriété canonique PidTagAddressBookChooseDirectoryAutomatically</span><span class="sxs-lookup"><span data-stu-id="5621d-103">PidTagAddressBookChooseDirectoryAutomatically Canonical Property</span></span>

  
  
<span data-ttu-id="5621d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5621d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5621d-105">Permet à Microsoft Outlook 2010 et Microsoft Outlook 2013 de choisir la liste d’adresses globale (GAL) plus appropriée ou le dossier de contacts pour la boîte aux lettres en cours.</span><span class="sxs-lookup"><span data-stu-id="5621d-105">Enables Microsoft Outlook 2010 and Microsoft Outlook 2013 to choose the most appropriate global address list (GAL) or contact folder for the current mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5621d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5621d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5621d-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="5621d-107">PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY</span></span>  <br/> |
|<span data-ttu-id="5621d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5621d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5621d-109">0x3D1C000B</span><span class="sxs-lookup"><span data-stu-id="5621d-109">0x3D1C000B</span></span>  <br/> |
|<span data-ttu-id="5621d-110">Type de propriété :</span><span class="sxs-lookup"><span data-stu-id="5621d-110">Property type:</span></span>  <br/> |<span data-ttu-id="5621d-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5621d-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5621d-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="5621d-112">Area:</span></span>  <br/> |<span data-ttu-id="5621d-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="5621d-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5621d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5621d-114">Remarks</span></span>

<span data-ttu-id="5621d-115">Cette propriété correspond au paramètre **d’Accepter automatiquement** dans la boîte de dialogue Options de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="5621d-115">This property corresponds to the **Choose automatically** setting in the Address Book Options dialog.</span></span> <span data-ttu-id="5621d-116">Lorsque cette propriété existe dans la section profil IID_CAPONE_PROF et est définie sur **true**, le carnet d’adresses, boîte de dialogue par défaut, le conteneur spécifié par la méthode [SetDefaultDir](iaddrbook-setdefaultdir.md) n’est plus mais choisit un carnet d’adresses qui Outlook 2010 ou Outlook 2013 estime appropriée pour le contexte dans lequel la boîte de dialogue a été affiché.</span><span class="sxs-lookup"><span data-stu-id="5621d-116">When this property exists in the IID_CAPONE_PROF profile section and is set to **true**, the Address Book dialog no longer defaults to the container specified by the [SetDefaultDir](iaddrbook-setdefaultdir.md) method, but chooses an address book that Outlook 2010 or Outlook 2013 considers appropriate for the context in which the dialog was displayed.</span></span> <span data-ttu-id="5621d-117">Notez que cela peut entraîner une mauvaise expérience pour les fournisseurs de carnet d’adresses tiers.</span><span class="sxs-lookup"><span data-stu-id="5621d-117">Note that this may result in a poor experience for third-party address book providers.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5621d-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5621d-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5621d-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5621d-119">Header files</span></span>

<span data-ttu-id="5621d-120">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="5621d-120">Mapitags.h</span></span>
  
> <span data-ttu-id="5621d-121">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="5621d-121">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="5621d-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5621d-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="5621d-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5621d-123">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5621d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5621d-124">See also</span></span>



[<span data-ttu-id="5621d-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5621d-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5621d-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5621d-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5621d-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="5621d-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="5621d-128">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5621d-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5621d-129">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="5621d-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

