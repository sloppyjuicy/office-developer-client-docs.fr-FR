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
# <a name="exchange_store_version_num"></a><span data-ttu-id="126bf-103">EXCHANGE_STORE_VERSION_NUM</span><span class="sxs-lookup"><span data-stu-id="126bf-103">EXCHANGE_STORE_VERSION_NUM</span></span>

  
  
<span data-ttu-id="126bf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="126bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="126bf-105">Stocke les informations de version des Microsoft Exchange Server comptes d’un Microsoft Office Outlook sont connectés.</span><span class="sxs-lookup"><span data-stu-id="126bf-105">Stores version information for the Microsoft Exchange Server that accounts in a Microsoft Office Outlook profile are connected to.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="126bf-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="126bf-106">Quick info</span></span>

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a><span data-ttu-id="126bf-107">Membres</span><span class="sxs-lookup"><span data-stu-id="126bf-107">Members</span></span>

 <span data-ttu-id="126bf-108">_wMajorVersion_</span><span class="sxs-lookup"><span data-stu-id="126bf-108">_wMajorVersion_</span></span>
  
- <span data-ttu-id="126bf-109">Numéro de version principal généralement incrémenté lorsqu’une version contient d’importantes nouvelles fonctionnalités et modifications de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="126bf-109">Major version number that is generally incremented when a release contains significant new features and changes in functionality.</span></span>
    
 <span data-ttu-id="126bf-110">_wMinorVersion_</span><span class="sxs-lookup"><span data-stu-id="126bf-110">_wMinorVersion_</span></span>
  
- <span data-ttu-id="126bf-111">Numéro de version mineure qui correspond à un numéro de version majeur spécifique et qui est généralement incrémenté lorsqu’une version contient de nouvelles fonctionnalités mineures ou des correctifs significatifs.</span><span class="sxs-lookup"><span data-stu-id="126bf-111">Minor version number that corresponds to a specific major version number and that is generally incremented when a release contains minor new features or significant fixes.</span></span>
    
 <span data-ttu-id="126bf-112">_wBuild_</span><span class="sxs-lookup"><span data-stu-id="126bf-112">_wBuild_</span></span>
  
- <span data-ttu-id="126bf-113">Numéro de build principal qui correspond à des numéros de version principaux et mineurs spécifiques et qui est généralement incrémenté dans une version interne qui contient de nouvelles fonctionnalités ou correctifs.</span><span class="sxs-lookup"><span data-stu-id="126bf-113">Major build number that corresponds to specific major and minor version numbers and that is generally incremented in an internal release that contains new features or fixes.</span></span> <span data-ttu-id="126bf-114">Cette valeur est également incrémentée lorsque la publication est une branche de code interne majeure ou un jalon, tel qu’un candidat à la publication.</span><span class="sxs-lookup"><span data-stu-id="126bf-114">This value is also incremented when the release is a major internal code branch or milestone, such as a release candidate.</span></span>
    
 <span data-ttu-id="126bf-115">_wMinorBuild_</span><span class="sxs-lookup"><span data-stu-id="126bf-115">_wMinorBuild_</span></span>
  
- <span data-ttu-id="126bf-116">Numéro de build mineure généralement incrémenté dans une version interne qui contient de nouvelles fonctionnalités ou correctifs correspondant à une build majeure spécifique qui indique une branche de code majeure ou un jalon.</span><span class="sxs-lookup"><span data-stu-id="126bf-116">Minor build number that is generally incremented in an internal release that contains new features or fixes corresponding to a specific major build that denotes a major code branch or milestone.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="126bf-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="126bf-117">See also</span></span>



[<span data-ttu-id="126bf-118">À propos des ajouts MAPI</span><span class="sxs-lookup"><span data-stu-id="126bf-118">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="126bf-119">Propriété canonique PidTagProfileServerFullVersion</span><span class="sxs-lookup"><span data-stu-id="126bf-119">PidTagProfileServerFullVersion Canonical Property</span></span>](pidtagprofileserverfullversion-canonical-property.md)

