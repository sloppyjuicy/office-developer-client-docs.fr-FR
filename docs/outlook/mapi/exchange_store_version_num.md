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
ms.openlocfilehash: bf60b12a6e4575d3504a112aa2b54fb8c4ae23c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433723"
---
# <a name="exchangestoreversionnum"></a><span data-ttu-id="92b9c-103">EXCHANGE_STORE_VERSION_NUM</span><span class="sxs-lookup"><span data-stu-id="92b9c-103">EXCHANGE_STORE_VERSION_NUM</span></span>

  
  
<span data-ttu-id="92b9c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92b9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92b9c-105">Stocke les informations relatives à la version du serveur Microsoft Exchange que les comptes dans un profil Microsoft Office Outlook sont connectés à.</span><span class="sxs-lookup"><span data-stu-id="92b9c-105">Stores version information for the Microsoft Exchange Server that accounts in a Microsoft Office Outlook profile are connected to.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="92b9c-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="92b9c-106">Quick info</span></span>

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a><span data-ttu-id="92b9c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="92b9c-107">Members</span></span>

 <span data-ttu-id="92b9c-108">_wMajorVersion_</span><span class="sxs-lookup"><span data-stu-id="92b9c-108">_wMajorVersion_</span></span>
  
- <span data-ttu-id="92b9c-109">Numéro de version majeure généralement incrémenté lorsqu'une publication contient de nouvelles fonctionnalités et des modifications de fonctionnalité importantes.</span><span class="sxs-lookup"><span data-stu-id="92b9c-109">Major version number that is generally incremented when a release contains significant new features and changes in functionality.</span></span>
    
 <span data-ttu-id="92b9c-110">_wMinorVersion_</span><span class="sxs-lookup"><span data-stu-id="92b9c-110">_wMinorVersion_</span></span>
  
- <span data-ttu-id="92b9c-111">Numéro de version mineure correspondant à un numéro de version principal spécifique et généralement incrémenté lorsqu'une publication contient de nouvelles fonctionnalités mineures ou des correctifs importants.</span><span class="sxs-lookup"><span data-stu-id="92b9c-111">Minor version number that corresponds to a specific major version number and that is generally incremented when a release contains minor new features or significant fixes.</span></span>
    
 <span data-ttu-id="92b9c-112">_wBuild_</span><span class="sxs-lookup"><span data-stu-id="92b9c-112">_wBuild_</span></span>
  
- <span data-ttu-id="92b9c-113">Numéro de build majeur correspondant à des numéros de version principaux et mineurs spécifiques, généralement incrémenté dans une version interne qui contient de nouvelles fonctionnalités ou des correctifs.</span><span class="sxs-lookup"><span data-stu-id="92b9c-113">Major build number that corresponds to specific major and minor version numbers and that is generally incremented in an internal release that contains new features or fixes.</span></span> <span data-ttu-id="92b9c-114">Cette valeur est également incrémentée lorsque la version est une branche de code interne majeure ou une étape majeure, telle qu'une version Release candidate.</span><span class="sxs-lookup"><span data-stu-id="92b9c-114">This value is also incremented when the release is a major internal code branch or milestone, such as a release candidate.</span></span>
    
 <span data-ttu-id="92b9c-115">_wMinorBuild_</span><span class="sxs-lookup"><span data-stu-id="92b9c-115">_wMinorBuild_</span></span>
  
- <span data-ttu-id="92b9c-116">Numéro de version mineure généralement incrémenté dans une version interne qui contient de nouvelles fonctionnalités ou des correctifs correspondant à une build majeure spécifique qui désigne une branche ou un jalon de code principal.</span><span class="sxs-lookup"><span data-stu-id="92b9c-116">Minor build number that is generally incremented in an internal release that contains new features or fixes corresponding to a specific major build that denotes a major code branch or milestone.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92b9c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92b9c-117">See also</span></span>



[<span data-ttu-id="92b9c-118">À propos des ajouts MAPI</span><span class="sxs-lookup"><span data-stu-id="92b9c-118">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="92b9c-119">Propriété canonique PidTagProfileServerFullVersion</span><span class="sxs-lookup"><span data-stu-id="92b9c-119">PidTagProfileServerFullVersion Canonical Property</span></span>](pidtagprofileserverfullversion-canonical-property.md)

