---
title: IMAPISupportModifyStatusRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyStatusRow
api_type:
- COM
ms.assetid: a304ca8f-e404-4535-be76-0b673f2061a0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8c76e6059670e782ea6530ec8e94f77abfe5b9fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417160"
---
# <a name="imapisupportmodifystatusrow"></a><span data-ttu-id="219d7-103">IMAPISupport::ModifyStatusRow</span><span class="sxs-lookup"><span data-stu-id="219d7-103">IMAPISupport::ModifyStatusRow</span></span>

  
  
<span data-ttu-id="219d7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="219d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="219d7-105">Modifie le tableau d’état en ajoutant une nouvelle ligne ou en modifiant une ligne existante.</span><span class="sxs-lookup"><span data-stu-id="219d7-105">Modifies the status table by adding a new row or modifying an existing row.</span></span>
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="219d7-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="219d7-106">Parameters</span></span>

 <span data-ttu-id="219d7-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="219d7-107">_cValues_</span></span>
  
> <span data-ttu-id="219d7-108">[in] Nombre de propriétés à inclure dans la ligne du tableau d’état nouveau ou modifié.</span><span class="sxs-lookup"><span data-stu-id="219d7-108">[in] The count of properties to be included in the new or modified status table row.</span></span> 
    
 <span data-ttu-id="219d7-109">_lpColumnVals_</span><span class="sxs-lookup"><span data-stu-id="219d7-109">_lpColumnVals_</span></span>
  
> <span data-ttu-id="219d7-110">[in] Pointeur vers un tableau de valeurs de propriété qui décrivent les propriétés à inclure en tant que colonnes dans la ligne du tableau d’état nouveau ou modifié.</span><span class="sxs-lookup"><span data-stu-id="219d7-110">[in] A pointer to an array of property values that describe the properties to be included as columns in the new or modified status table row.</span></span>
    
 <span data-ttu-id="219d7-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="219d7-111">_ulFlags_</span></span>
  
> <span data-ttu-id="219d7-112">[in] Masque de bits d’indicateurs qui contrôle le traitement des informations qui définissent la ligne de tableau d’état.</span><span class="sxs-lookup"><span data-stu-id="219d7-112">[in] A bitmask of flags that controls how information that defines the status table row is processed.</span></span> <span data-ttu-id="219d7-113">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="219d7-113">The following flag can be set:</span></span>
    
<span data-ttu-id="219d7-114">STATUSROW_UPDATE</span><span class="sxs-lookup"><span data-stu-id="219d7-114">STATUSROW_UPDATE</span></span> 
  
> <span data-ttu-id="219d7-115">Indique à MAPI de fusionner les propriétés incluses dans le tableau pointé par  _lpColumnVals_ avec une ligne de tableau d’état existante, plutôt que dans une nouvelle ligne.</span><span class="sxs-lookup"><span data-stu-id="219d7-115">Directs MAPI to merge the properties included in the array pointed to by  _lpColumnVals_ with an existing status table row, rather than in a new row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="219d7-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="219d7-116">Return value</span></span>

<span data-ttu-id="219d7-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="219d7-117">S_OK</span></span> 
  
> <span data-ttu-id="219d7-118">La table d’état a été correctement mise à jour.</span><span class="sxs-lookup"><span data-stu-id="219d7-118">The status table was successfully updated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="219d7-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="219d7-119">Remarks</span></span>

<span data-ttu-id="219d7-120">La **méthode IMAPISupport::ModifyStatusRow** est implémentée pour tous les objets de prise en charge du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="219d7-120">The **IMAPISupport::ModifyStatusRow** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="219d7-121">Les fournisseurs de services **appellent ModifyStatusRow** au moment de l’ouverture de session pour ajouter une ligne à la table d’état et à d’autres moments de la session pour mettre à jour la ligne.</span><span class="sxs-lookup"><span data-stu-id="219d7-121">Service providers call **ModifyStatusRow** at logon time to add a row to the status table and at other times during the session to update the row.</span></span> <span data-ttu-id="219d7-122">**ModifyStatusRow fournit** à MAPI les informations nécessaires pour créer la table d’état.</span><span class="sxs-lookup"><span data-stu-id="219d7-122">**ModifyStatusRow** provides MAPI with the information necessary to build the status table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="219d7-123">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="219d7-123">Notes to callers</span></span>

<span data-ttu-id="219d7-124">Définissez l STATUSROW_UPDATE lorsque vous appelez **ModifyStatusRow** pour apporter des modifications aux propriétés de la ligne de votre table d’état existante.</span><span class="sxs-lookup"><span data-stu-id="219d7-124">Set the STATUSROW_UPDATE flag when you call **ModifyStatusRow** to make changes to the properties in your existing status table row.</span></span> <span data-ttu-id="219d7-125">Cela informe MAPI que seules les colonnes modifiées sont passées dans le _paramètre lpColumnVals._</span><span class="sxs-lookup"><span data-stu-id="219d7-125">Doing so informs MAPI that only the columns being changed are passed in the  _lpColumnVals_ parameter.</span></span> 
  
<span data-ttu-id="219d7-126">Les clients peuvent utiliser les informations de la table d’état pour accéder à votre objet d’état.</span><span class="sxs-lookup"><span data-stu-id="219d7-126">Clients can use the information in the status table to access your status object.</span></span> 
  
<span data-ttu-id="219d7-127">Pour obtenir la liste complète des colonnes que vous devez inclure dans la ligne de votre tableau d’état, voir [Tableaux d’état.](status-tables.md)</span><span class="sxs-lookup"><span data-stu-id="219d7-127">For a complete list of columns that you should include in your status table row, see [Status Tables](status-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="219d7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="219d7-128">See also</span></span>



[<span data-ttu-id="219d7-129">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="219d7-129">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

