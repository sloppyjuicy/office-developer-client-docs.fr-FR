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
ms.openlocfilehash: fea2b496a34d7aa7f9469158fae14daf6a770608
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787178"
---
# <a name="sizeddtblcombobox"></a><span data-ttu-id="a6814-103">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="a6814-103">SizedDtblComboBox</span></span>
 
<span data-ttu-id="a6814-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a6814-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a6814-105">Crée une structure nommée qui inclut une structure [DTBLCOMBOBOX](dtblcombobox.md) pour la description d’un contrôle de zone de liste déroulante et le nombre maximal de caractères pouvant être entré dans le contrôle d’édition associé.</span><span class="sxs-lookup"><span data-stu-id="a6814-105">Creates a named structure that includes a [DTBLCOMBOBOX](dtblcombobox.md) structure for describing a combo box control and the maximum number of characters that can be entered in the associated edit control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6814-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a6814-106">Header file:</span></span>  <br/> |<span data-ttu-id="a6814-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a6814-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a6814-108">Structure connexe :</span><span class="sxs-lookup"><span data-stu-id="a6814-108">Related structure:</span></span>  <br/> |<span data-ttu-id="a6814-109">**DTBLCOMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="a6814-109">**DTBLCOMBOBOX**</span></span> <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="a6814-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6814-110">Parameters</span></span>

<span data-ttu-id="a6814-111">_n_</span><span class="sxs-lookup"><span data-stu-id="a6814-111">_n_</span></span>
  
> <span data-ttu-id="a6814-112">Nombre de caractères pouvant figurer dans la liste déroulante du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="a6814-112">Number of characters that can be entered in the combo box's edit control.</span></span> 
    
<span data-ttu-id="a6814-113">_u_</span><span class="sxs-lookup"><span data-stu-id="a6814-113">_u_</span></span>
  
> <span data-ttu-id="a6814-114">Nom de la nouvelle structure.</span><span class="sxs-lookup"><span data-stu-id="a6814-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6814-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="a6814-115">Remarks</span></span>

<span data-ttu-id="a6814-116">La macro **SizedDtblComboBox** vous permet de définir une zone de liste déroulante lorsque la longueur de la chaîne de caractères activé est connue.</span><span class="sxs-lookup"><span data-stu-id="a6814-116">The **SizedDtblComboBox** macro lets you define a combo box when the length of the enabled character string is known.</span></span> <span data-ttu-id="a6814-117">La nouvelle structure est créée avec les membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a6814-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="a6814-118">Pour utiliser un pointeur vers la structure obtenue à partir de la macro **SizedDtblComboBox** comme un pointeur de structure **DTBLCOMBOBOX** , effectuer le cast suivant :</span><span class="sxs-lookup"><span data-stu-id="a6814-118">To use a pointer to the resulting structure from the **SizedDtblComboBox** macro as a **DTBLCOMBOBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a><span data-ttu-id="a6814-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6814-119">See also</span></span>

- [<span data-ttu-id="a6814-120">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="a6814-120">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="a6814-121">Macros relatives aux Structures</span><span class="sxs-lookup"><span data-stu-id="a6814-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

