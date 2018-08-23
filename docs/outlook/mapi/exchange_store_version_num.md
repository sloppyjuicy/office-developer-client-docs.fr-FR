---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 152afd68bea44f3485b2cc566f3f0d2768590704
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594473"
---
# <a name="exchangestoreversionnum"></a><span data-ttu-id="2cdff-103">EXCHANGE_STORE_VERSION_NUM</span><span class="sxs-lookup"><span data-stu-id="2cdff-103">EXCHANGE_STORE_VERSION_NUM</span></span>

  
  
<span data-ttu-id="2cdff-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2cdff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2cdff-105">Stocke les informations de version de Microsoft Exchange Server dans un profil de Microsoft Office Outlook, les comptes connectés à.</span><span class="sxs-lookup"><span data-stu-id="2cdff-105">Stores version information for the Microsoft Exchange Server that accounts in a Microsoft Office Outlook profile are connected to.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2cdff-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="2cdff-106">Quick info</span></span>

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a><span data-ttu-id="2cdff-107">Members</span><span class="sxs-lookup"><span data-stu-id="2cdff-107">Members</span></span>

 <span data-ttu-id="2cdff-108">_wMajorVersion_</span><span class="sxs-lookup"><span data-stu-id="2cdff-108">_wMajorVersion_</span></span>
  
- <span data-ttu-id="2cdff-109">Numéro de version principal est généralement incrémenté lorsqu’une version contient importantes nouvelles fonctionnalités et modifications de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="2cdff-109">Major version number that is generally incremented when a release contains significant new features and changes in functionality.</span></span>
    
 <span data-ttu-id="2cdff-110">_wMinorVersion_</span><span class="sxs-lookup"><span data-stu-id="2cdff-110">_wMinorVersion_</span></span>
  
- <span data-ttu-id="2cdff-111">Numéro de version secondaire qui correspond à un numéro de version majeure et qui est généralement incrémenté lorsqu’une version contient les nouvelles fonctionnalités secondaires ou correctifs importants.</span><span class="sxs-lookup"><span data-stu-id="2cdff-111">Minor version number that corresponds to a specific major version number and that is generally incremented when a release contains minor new features or significant fixes.</span></span>
    
 <span data-ttu-id="2cdff-112">_wBuild_</span><span class="sxs-lookup"><span data-stu-id="2cdff-112">_wBuild_</span></span>
  
- <span data-ttu-id="2cdff-113">Numéro de version majeur qui correspond aux numéros de version principale et secondaire spécifique et qui est généralement incrémentée dans une version interne qui contient des correctifs ou des nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="2cdff-113">Major build number that corresponds to specific major and minor version numbers and that is generally incremented in an internal release that contains new features or fixes.</span></span> <span data-ttu-id="2cdff-114">Cette valeur est également incrémentée à la version est une branche de code interne principale ou un jalon, par exemple une version release candidate.</span><span class="sxs-lookup"><span data-stu-id="2cdff-114">This value is also incremented when the release is a major internal code branch or milestone, such as a release candidate.</span></span>
    
 <span data-ttu-id="2cdff-115">_wMinorBuild_</span><span class="sxs-lookup"><span data-stu-id="2cdff-115">_wMinorBuild_</span></span>
  
- <span data-ttu-id="2cdff-116">Numéro de version secondaire est incrémentée généralement dans une version interne qui contient les nouvelles fonctionnalités ou corrige correspondant à une version principale spécifique qui indique une branche de code principal ou un jalon.</span><span class="sxs-lookup"><span data-stu-id="2cdff-116">Minor build number that is generally incremented in an internal release that contains new features or fixes corresponding to a specific major build that denotes a major code branch or milestone.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2cdff-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cdff-117">See also</span></span>



[<span data-ttu-id="2cdff-118">À propos des ajouts MAPI</span><span class="sxs-lookup"><span data-stu-id="2cdff-118">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="2cdff-119">Propriété canonique PidTagProfileServerFullVersion</span><span class="sxs-lookup"><span data-stu-id="2cdff-119">PidTagProfileServerFullVersion Canonical Property</span></span>](pidtagprofileserverfullversion-canonical-property.md)

