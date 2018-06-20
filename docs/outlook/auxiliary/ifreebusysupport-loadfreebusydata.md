---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Renvoie, pour chaque utilisateur spécifié, une interface pour énumérer les informations de disponibilité des blocs de données au sein d’une plage de temps.
ms.openlocfilehash: 9af5a40da9f0a831de7346b44cee9ca004c02300
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782586"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="f625b-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="f625b-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="f625b-104">Renvoie, pour chaque utilisateur spécifié, une interface pour énumérer les informations de disponibilité des blocs de données au sein d’une plage de temps.</span><span class="sxs-lookup"><span data-stu-id="f625b-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="f625b-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="f625b-105">Quick info</span></span>

<span data-ttu-id="f625b-106">Voir [IFreeBusySupport](ifreebusysupport.md).</span><span class="sxs-lookup"><span data-stu-id="f625b-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="f625b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f625b-107">Parameters</span></span>

<span data-ttu-id="f625b-108">_cMax_</span><span class="sxs-lookup"><span data-stu-id="f625b-108">_cMax_</span></span>
  
> <span data-ttu-id="f625b-109">[in] Le nombre d’interfaces [IFreeBusyData](ifreebusydata.md) à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="f625b-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="f625b-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="f625b-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="f625b-111">[in] Le tableau de disponibilité pour les utilisateurs à récupérer des données pour.</span><span class="sxs-lookup"><span data-stu-id="f625b-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="f625b-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="f625b-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="f625b-113">[in] [out] Tableau des interfaces **IFreeBusyData** qui correspondent au tableau de structures [FBUser](fbuser.md) _rgfbuser_ .</span><span class="sxs-lookup"><span data-stu-id="f625b-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="f625b-114">Ce tableau de pointeurs est alloué par l’appelant et libéré par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="f625b-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="f625b-115">Les interfaces réels vers lequel pointés sont libérées lorsque l’appelant est terminé avec eux.</span><span class="sxs-lookup"><span data-stu-id="f625b-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="f625b-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="f625b-116">_phrStatus_</span></span>
  
> <span data-ttu-id="f625b-117">[out] Le tableau de résultats **HRESULT** pour l’extraction de chaque interface **IFreeBusyData** correspondante.</span><span class="sxs-lookup"><span data-stu-id="f625b-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="f625b-118">La valeur peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="f625b-118">The value may be NULL.</span></span> <span data-ttu-id="f625b-119">Un résultat est défini à S_OK si correspondante _prgfbdata_ n’est valide.</span><span class="sxs-lookup"><span data-stu-id="f625b-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="f625b-120">_pcRead_</span><span class="sxs-lookup"><span data-stu-id="f625b-120">_pcRead_</span></span>
  
>  <span data-ttu-id="f625b-121">[out] Le nombre d’utilisateurs pour lequel une interface **IFreeBusyData** a été détectée.</span><span class="sxs-lookup"><span data-stu-id="f625b-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="f625b-122">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="f625b-122">Return values</span></span>

<span data-ttu-id="f625b-123">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="f625b-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f625b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f625b-124">See also</span></span>

- [<span data-ttu-id="f625b-125">Constantes (disponibilité API)</span><span class="sxs-lookup"><span data-stu-id="f625b-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

