---
title: Propriété canonique PidTagProviderIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderIcon
api_type:
- COM
ms.assetid: 59c84b1f-13b5-484b-b703-2fb9fcc6c7eb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 55e6c8fb013e544ae04740aeaeb23ac23949cffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425637"
---
# <a name="pidtagprovidericon-canonical-property"></a><span data-ttu-id="1f670-103">Propriété canonique PidTagProviderIcon</span><span class="sxs-lookup"><span data-stu-id="1f670-103">PidTagProviderIcon Canonical Property</span></span>

  
  
<span data-ttu-id="1f670-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f670-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f670-105">Contient une chaîne Unicode qui spécifie une ou plusieurs icônes personnalisées à afficher pour un fournisseur MAPI dans la barre d’état Microsoft Office Outlook dans les états en ligne et hors connexion.</span><span class="sxs-lookup"><span data-stu-id="1f670-105">Contains a Unicode string that specifies a custom icon or icons to be displayed for a MAPI provider in the Microsoft Office Outlook status bar in both online and offline states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1f670-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1f670-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f670-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span><span class="sxs-lookup"><span data-stu-id="1f670-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span></span>  <br/> |
|<span data-ttu-id="1f670-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1f670-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f670-109">0x3417</span><span class="sxs-lookup"><span data-stu-id="1f670-109">0x3417</span></span>  <br/> |
|<span data-ttu-id="1f670-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1f670-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f670-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1f670-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1f670-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1f670-112">Area:</span></span>  <br/> |<span data-ttu-id="1f670-113">Magasin de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="1f670-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f670-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1f670-114">Remarks</span></span>

<span data-ttu-id="1f670-115">Ces propriétés spécifient le fichier de ressources qui contient une icône personnalisée qui représente un fournisseur MAPI dans un état en ligne, et éventuellement une autre icône personnalisée en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="1f670-115">These properties specify the resource file that contains a custom icon that represents a MAPI provider in an online state, and optionally, another custom icon in the offline state.</span></span> <span data-ttu-id="1f670-116">Outlook demande toujours ces propriétés dans la représentation Unicode.</span><span class="sxs-lookup"><span data-stu-id="1f670-116">Outlook always requests these properties in Unicode representation.</span></span> 
  
<span data-ttu-id="1f670-117">Par exemple, la valeur de propriété suivante indique à Outlook de charger l’ID d’icône 1001 à partir de la mymod32.dll de module et d’utiliser cette icône pour l’état en ligne `mymod32.dll,#1001` :</span><span class="sxs-lookup"><span data-stu-id="1f670-117">For example, the following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state:  `mymod32.dll,#1001`.</span></span> <span data-ttu-id="1f670-118">Étant donné qu’il n’existe aucune icône spécifique au fournisseur pour l’état hors connexion, dans ce cas, l’icône Outlook hors connexion standard est utilisée dans la barre d’état.</span><span class="sxs-lookup"><span data-stu-id="1f670-118">Since there is no provider-specific icon for the offline state, in this case, the standard Outlook offline icon is used in the status bar.</span></span> 
  
<span data-ttu-id="1f670-119">La valeur de propriété suivante indique à Outlook de charger l’ID d’icône 1001 à partir de l'mymod32.dll de module et d’utiliser cette icône pour l’état en ligne, ainsi que de charger l’ID d’icône 1002 à partir de ce même module à utiliser pour l’état hors connexion : `mymod32.dll,#1001,#1002`</span><span class="sxs-lookup"><span data-stu-id="1f670-119">The following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state, and to also load icon ID 1002 from this same module to be used for the offline state:  `mymod32.dll,#1001,#1002`.</span></span> <span data-ttu-id="1f670-120">Aucune Outlook’icône n’est utilisée dans la barre d’état.</span><span class="sxs-lookup"><span data-stu-id="1f670-120">No Outlook icon is used in the status bar.</span></span> 
  
<span data-ttu-id="1f670-121">Par défaut, si aucune icône personnalisée n’est spécifiée, le fournisseur est représenté par les Outlook par défaut pour l’état en ligne et l’état hors connexion.</span><span class="sxs-lookup"><span data-stu-id="1f670-121">By default, if no custom icons are specified, the provider is represented by the Outlook default icons for the online state and the offline state.</span></span> <span data-ttu-id="1f670-122">Le fournisseur peut éventuellement spécifier un nom d’affichage à afficher en adjacent à l’icône dans la barre d’état.</span><span class="sxs-lookup"><span data-stu-id="1f670-122">The provider can optionally specify a display name to be shown adjacent to the icon in the status bar.</span></span> <span data-ttu-id="1f670-123">Pour plus d’informations, **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1f670-123">For more information, see **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1f670-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1f670-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1f670-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1f670-125">Header files</span></span>

<span data-ttu-id="1f670-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f670-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f670-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1f670-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f670-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1f670-128">Mapitags.h</span></span>
  
> <span data-ttu-id="1f670-129">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="1f670-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f670-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f670-130">See also</span></span>



[<span data-ttu-id="1f670-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1f670-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f670-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1f670-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f670-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1f670-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f670-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1f670-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

