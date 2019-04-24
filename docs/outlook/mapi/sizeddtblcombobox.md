---
title: SizedDtblComboBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblComboBox
api_type:
- COM
ms.assetid: 1e5ea9f2-1029-4584-845a-890d3e956036
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8861c8f86eaab6defb270b673e0ee200446aedb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282823"
---
# <a name="sizeddtblcombobox"></a><span data-ttu-id="3fdf9-103">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="3fdf9-103">SizedDtblComboBox</span></span>
 
<span data-ttu-id="3fdf9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fdf9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fdf9-105">Crée une structure nommée qui inclut une structure [DTBLCOMBOBOX](dtblcombobox.md) pour décrire un contrôle de zone de liste déroulante et le nombre maximal de caractères pouvant être entrés dans le contrôle d'édition associé.</span><span class="sxs-lookup"><span data-stu-id="3fdf9-105">Creates a named structure that includes a [DTBLCOMBOBOX](dtblcombobox.md) structure for describing a combo box control and the maximum number of characters that can be entered in the associated edit control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3fdf9-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="3fdf9-106">Header file:</span></span>  <br/> |<span data-ttu-id="3fdf9-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3fdf9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3fdf9-108">Structure associée:</span><span class="sxs-lookup"><span data-stu-id="3fdf9-108">Related structure:</span></span>  <br/> |<span data-ttu-id="3fdf9-109">**DTBLCOMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="3fdf9-109">**DTBLCOMBOBOX**</span></span> <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="3fdf9-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3fdf9-110">Parameters</span></span>

<span data-ttu-id="3fdf9-111">_n_</span><span class="sxs-lookup"><span data-stu-id="3fdf9-111">_n_</span></span>
  
> <span data-ttu-id="3fdf9-112">Nombre de caractères pouvant être entrés dans le contrôle d'édition de la zone de liste modifiable.</span><span class="sxs-lookup"><span data-stu-id="3fdf9-112">Number of characters that can be entered in the combo box's edit control.</span></span> 
    
<span data-ttu-id="3fdf9-113">_u_</span><span class="sxs-lookup"><span data-stu-id="3fdf9-113">_u_</span></span>
  
> <span data-ttu-id="3fdf9-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="3fdf9-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3fdf9-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="3fdf9-115">Remarks</span></span>

<span data-ttu-id="3fdf9-116">La macro **SizedDtblComboBox** vous permet de définir une zone de liste déroulante lorsque la longueur de la chaîne de caractères activée est connue.</span><span class="sxs-lookup"><span data-stu-id="3fdf9-116">The **SizedDtblComboBox** macro lets you define a combo box when the length of the enabled character string is known.</span></span> <span data-ttu-id="3fdf9-117">La nouvelle structure est créée avec les membres suivants:</span><span class="sxs-lookup"><span data-stu-id="3fdf9-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="3fdf9-118">Pour utiliser un pointeur vers la structure obtenue à partir de la macro **SizedDtblComboBox** en tant que pointeur de structure **DTBLCOMBOBOX** , effectuez la conversion suivante:</span><span class="sxs-lookup"><span data-stu-id="3fdf9-118">To use a pointer to the resulting structure from the **SizedDtblComboBox** macro as a **DTBLCOMBOBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a><span data-ttu-id="3fdf9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fdf9-119">See also</span></span>

- [<span data-ttu-id="3fdf9-120">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="3fdf9-120">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="3fdf9-121">Macros liées aux structures</span><span class="sxs-lookup"><span data-stu-id="3fdf9-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

