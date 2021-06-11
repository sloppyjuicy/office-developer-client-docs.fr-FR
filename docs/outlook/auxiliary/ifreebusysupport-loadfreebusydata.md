---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Renvoie, pour chaque utilisateur spécifié, une interface pour l’éumation des blocs de données de libre/occupé dans un délai.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411231"
---
# <a name="ifreebusysupportloadfreebusydata"></a><span data-ttu-id="4df9c-103">IFreeBusySupport::LoadFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="4df9c-103">IFreeBusySupport::LoadFreeBusyData</span></span>

<span data-ttu-id="4df9c-104">Renvoie, pour chaque utilisateur spécifié, une interface pour l’éumation des blocs de données de libre/occupé dans un délai.</span><span class="sxs-lookup"><span data-stu-id="4df9c-104">Returns, for each specified user, an interface for enumerating free/busy blocks of data within a time range.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4df9c-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="4df9c-105">Quick info</span></span>

<span data-ttu-id="4df9c-106">Voir [IFreeBusySupport](ifreebusysupport.md).</span><span class="sxs-lookup"><span data-stu-id="4df9c-106">See [IFreeBusySupport](ifreebusysupport.md).</span></span>
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a><span data-ttu-id="4df9c-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="4df9c-107">Parameters</span></span>

<span data-ttu-id="4df9c-108">_cMax_</span><span class="sxs-lookup"><span data-stu-id="4df9c-108">_cMax_</span></span>
  
> <span data-ttu-id="4df9c-109">[in] Nombre d’interfaces [IFreeBusyData](ifreebusydata.md) à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="4df9c-109">[in] The number of [IFreeBusyData](ifreebusydata.md) interfaces to return.</span></span> 
    
<span data-ttu-id="4df9c-110">_rgfbuser_</span><span class="sxs-lookup"><span data-stu-id="4df9c-110">_rgfbuser_</span></span>
  
> <span data-ttu-id="4df9c-111">[in] Tableau des utilisateurs de libre/occupé pour qui récupérer des données.</span><span class="sxs-lookup"><span data-stu-id="4df9c-111">[in] The array of free/busy users to retrieve data for.</span></span>
    
<span data-ttu-id="4df9c-112">_prgfbdata_</span><span class="sxs-lookup"><span data-stu-id="4df9c-112">_prgfbdata_</span></span>
  
> <span data-ttu-id="4df9c-113">[in] [out] Tableau des interfaces **IFreeBusyData** qui correspondent au tableau _rgfbuser_ des structures [FBUser.](fbuser.md)</span><span class="sxs-lookup"><span data-stu-id="4df9c-113">[in][out] The array of **IFreeBusyData** interfaces that correspond to the  _rgfbuser_ array of [FBUser](fbuser.md) structures.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="4df9c-114">Ce tableau de pointeurs est alloué par l’appelant et libéré par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="4df9c-114">This array of pointers is allocated by the caller and freed by the caller.</span></span> <span data-ttu-id="4df9c-115">Les interfaces réelles pointées vers sont libérées lorsque l’appelant a terminé de les utiliser.</span><span class="sxs-lookup"><span data-stu-id="4df9c-115">The actual interfaces pointed to are released when the caller is done with them.</span></span> 
  
<span data-ttu-id="4df9c-116">_phrStatus_</span><span class="sxs-lookup"><span data-stu-id="4df9c-116">_phrStatus_</span></span>
  
> <span data-ttu-id="4df9c-117">[out] Tableau des résultats **HRESULT** pour la récupération de chaque interface **IFreeBusyData** correspondante.</span><span class="sxs-lookup"><span data-stu-id="4df9c-117">[out] The array of **HRESULT** results for retrieving each corresponding **IFreeBusyData** interface.</span></span> <span data-ttu-id="4df9c-118">La valeur peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="4df9c-118">The value may be NULL.</span></span> <span data-ttu-id="4df9c-119">Un résultat est S_OK si  _prgfbdata_ est valide.</span><span class="sxs-lookup"><span data-stu-id="4df9c-119">A result is set to S_OK if corresponding  _prgfbdata_ is valid.</span></span> 
    
<span data-ttu-id="4df9c-120">_pcRead_</span><span class="sxs-lookup"><span data-stu-id="4df9c-120">_pcRead_</span></span>
  
>  <span data-ttu-id="4df9c-121">[out] Nombre réel d’utilisateurs pour lesquels une interface **IFreeBusyData** a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="4df9c-121">[out] The actual number of users for which an **IFreeBusyData** interface has been found.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="4df9c-122">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="4df9c-122">Return values</span></span>

<span data-ttu-id="4df9c-123">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="4df9c-123">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4df9c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4df9c-124">See also</span></span>

- [<span data-ttu-id="4df9c-125">Constantes (API de libre/occupé)</span><span class="sxs-lookup"><span data-stu-id="4df9c-125">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)

