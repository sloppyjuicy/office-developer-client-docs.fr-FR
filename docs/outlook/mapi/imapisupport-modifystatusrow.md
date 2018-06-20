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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 24718c50d02da5d60a6594f56ea6100650fe9f1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783994"
---
# <a name="imapisupportmodifystatusrow"></a><span data-ttu-id="7902c-103">IMAPISupport::ModifyStatusRow</span><span class="sxs-lookup"><span data-stu-id="7902c-103">IMAPISupport::ModifyStatusRow</span></span>

  
  
<span data-ttu-id="7902c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7902c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7902c-105">Modifie la table d’état en ajoutant une nouvelle ligne ou de modification d’une ligne existante.</span><span class="sxs-lookup"><span data-stu-id="7902c-105">Modifies the status table by adding a new row or modifying an existing row.</span></span>
  
```cpp
HRESULT ModifyStatusRow(
ULONG cValues,
LPSPropValue lpColumnVals,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="7902c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7902c-106">Parameters</span></span>

 <span data-ttu-id="7902c-107">_cValues_</span><span class="sxs-lookup"><span data-stu-id="7902c-107">_cValues_</span></span>
  
> <span data-ttu-id="7902c-108">[in] Le nombre de propriétés à inclure dans la ligne de tableau état créé ou modifié.</span><span class="sxs-lookup"><span data-stu-id="7902c-108">[in] The count of properties to be included in the new or modified status table row.</span></span> 
    
 <span data-ttu-id="7902c-109">_lpColumnVals_</span><span class="sxs-lookup"><span data-stu-id="7902c-109">_lpColumnVals_</span></span>
  
> <span data-ttu-id="7902c-110">[in] Pointeur vers un tableau de valeurs de propriété qui décrivent les propriétés à inclure en tant que colonnes dans la ligne de tableau état créé ou modifié.</span><span class="sxs-lookup"><span data-stu-id="7902c-110">[in] A pointer to an array of property values that describe the properties to be included as columns in the new or modified status table row.</span></span>
    
 <span data-ttu-id="7902c-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7902c-111">_ulFlags_</span></span>
  
> <span data-ttu-id="7902c-112">[in] Masque de bits d’indicateurs qui contrôle le mode de traitement des informations qui définissent la ligne table d’état.</span><span class="sxs-lookup"><span data-stu-id="7902c-112">[in] A bitmask of flags that controls how information that defines the status table row is processed.</span></span> <span data-ttu-id="7902c-113">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="7902c-113">The following flag can be set:</span></span>
    
<span data-ttu-id="7902c-114">STATUSROW_UPDATE</span><span class="sxs-lookup"><span data-stu-id="7902c-114">STATUSROW_UPDATE</span></span> 
  
> <span data-ttu-id="7902c-115">Indique à MAPI pour fusionner les propriétés incluses dans le tableau vers lequel pointe _lpColumnVals_ avec une ligne de tableau d’état existante, plutôt que dans une nouvelle ligne.</span><span class="sxs-lookup"><span data-stu-id="7902c-115">Directs MAPI to merge the properties included in the array pointed to by  _lpColumnVals_ with an existing status table row, rather than in a new row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7902c-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="7902c-116">Return value</span></span>

<span data-ttu-id="7902c-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="7902c-117">S_OK</span></span> 
  
> <span data-ttu-id="7902c-118">La table d’état a été correctement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="7902c-118">The status table was successfully updated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7902c-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="7902c-119">Remarks</span></span>

<span data-ttu-id="7902c-120">La méthode **IMAPISupport::ModifyStatusRow** est implémentée pour tous les objets de prise en charge de fournisseur de service.</span><span class="sxs-lookup"><span data-stu-id="7902c-120">The **IMAPISupport::ModifyStatusRow** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="7902c-121">Fournisseurs de services d’appel **ModifyStatusRow** au moment de l’ouverture de session pour ajouter une ligne à la table d’état et à d’autres moments pendant la session de mise à jour de la ligne.</span><span class="sxs-lookup"><span data-stu-id="7902c-121">Service providers call **ModifyStatusRow** at logon time to add a row to the status table and at other times during the session to update the row.</span></span> <span data-ttu-id="7902c-122">**ModifyStatusRow** MAPI fournit les informations nécessaires pour créer la table d’état.</span><span class="sxs-lookup"><span data-stu-id="7902c-122">**ModifyStatusRow** provides MAPI with the information necessary to build the status table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7902c-123">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="7902c-123">Notes to callers</span></span>

<span data-ttu-id="7902c-124">Définir l’indicateur STATUSROW_UPDATE lorsque vous appelez **ModifyStatusRow** pour modifier les propriétés dans la ligne de tableau état existant.</span><span class="sxs-lookup"><span data-stu-id="7902c-124">Set the STATUSROW_UPDATE flag when you call **ModifyStatusRow** to make changes to the properties in your existing status table row.</span></span> <span data-ttu-id="7902c-125">Cela informe MAPI que seules les colonnes modifiées sont passés dans le paramètre _lpColumnVals_ .</span><span class="sxs-lookup"><span data-stu-id="7902c-125">Doing so informs MAPI that only the columns being changed are passed in the  _lpColumnVals_ parameter.</span></span> 
  
<span data-ttu-id="7902c-126">Clients peuvent utiliser les informations dans la table d’état pour accéder à votre objet d’état.</span><span class="sxs-lookup"><span data-stu-id="7902c-126">Clients can use the information in the status table to access your status object.</span></span> 
  
<span data-ttu-id="7902c-127">Pour obtenir une liste complète des colonnes que vous devez inclure dans votre ligne de tableau d’état, voir les [Tableaux d’état](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="7902c-127">For a complete list of columns that you should include in your status table row, see [Status Tables](status-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7902c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7902c-128">See also</span></span>



[<span data-ttu-id="7902c-129">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7902c-129">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

