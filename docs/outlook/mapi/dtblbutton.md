---
title: DTBLBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLBUTTON
api_type:
- COM
ms.assetid: 6058c78b-05d4-45a3-988c-1fbf8322125e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a8fa683fecd59ec813fee0c15d5b4f08084c645d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412785"
---
# <a name="dtblbutton"></a><span data-ttu-id="30526-103">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="30526-103">DTBLBUTTON</span></span>

  
  
<span data-ttu-id="30526-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30526-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30526-105">Contient des informations sur un contrôle de bouton pour une boîte de dialogue conçue à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="30526-105">Contains information about a button control for a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30526-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="30526-106">Header file:</span></span>  <br/> |<span data-ttu-id="30526-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30526-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="30526-108">Macro associée :</span><span class="sxs-lookup"><span data-stu-id="30526-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="30526-109">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="30526-109">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a><span data-ttu-id="30526-110">Members</span><span class="sxs-lookup"><span data-stu-id="30526-110">Members</span></span>

 <span data-ttu-id="30526-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="30526-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="30526-112">Position en mémoire de la chaîne de caractères affichée sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="30526-112">Position in memory of the character string that is displayed on the button.</span></span>
    
 <span data-ttu-id="30526-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="30526-113">**ulFlags**</span></span>
  
> <span data-ttu-id="30526-114">Masque de bits d’indicateurs utilisé pour désigner le format de l’étiquette pointée par le membre **ulbLpszLabel.**</span><span class="sxs-lookup"><span data-stu-id="30526-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="30526-115">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="30526-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="30526-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="30526-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="30526-117">L’étiquette est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="30526-117">The label is in Unicode format.</span></span> <span data-ttu-id="30526-118">Si l’MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="30526-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="30526-119">**ulPRControl**</span><span class="sxs-lookup"><span data-stu-id="30526-119">**ulPRControl**</span></span>
  
> <span data-ttu-id="30526-120">Balise de propriété pour une propriété de type PT_OBJECT qui implémente l’interface [IMAPIControl.](imapicontroliunknown.md)</span><span class="sxs-lookup"><span data-stu-id="30526-120">Property tag for a property of type PT_OBJECT that implements the [IMAPIControl](imapicontroliunknown.md) interface.</span></span> <span data-ttu-id="30526-121">Lorsque vous cliquez sur le bouton, MAPI appelle la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour l’implémentation [IMAPIProp](imapipropiunknown.md) de la table d’affichage afin de récupérer cette propriété.</span><span class="sxs-lookup"><span data-stu-id="30526-121">When the button is clicked, MAPI calls the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the display table's [IMAPIProp](imapipropiunknown.md) implementation to retrieve this property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="30526-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="30526-122">Remarks</span></span>

<span data-ttu-id="30526-123">Une structure **DTBLBUTTON** décrit un bouton d’un contrôle qui, lorsqu’on clique dessus, permet à un utilisateur de commencer une opération.</span><span class="sxs-lookup"><span data-stu-id="30526-123">A **DTBLBUTTON** structure describes a button a control that, when clicked, allows a user to begin an operation.</span></span> <span data-ttu-id="30526-124">En règle générale, le fait de cliquer sur un bouton entraîne l’affichage d’une boîte de dialogue modale ou l’appel d’une tâche par programme.</span><span class="sxs-lookup"><span data-stu-id="30526-124">Typically, clicking a button causes a modal dialog box to be displayed or a programmatic task to be invoked.</span></span> <span data-ttu-id="30526-125">Les fournisseurs de services peuvent implémenter n’importe quoi par le biais d’un contrôle de bouton.</span><span class="sxs-lookup"><span data-stu-id="30526-125">Service providers can implement anything through a button control.</span></span> <span data-ttu-id="30526-126">Si le bouton est censé effectuer une tâche basée sur les valeurs d’autres contrôles, ces contrôles doivent avoir DT_SET_IMMEDIATE indicateur.</span><span class="sxs-lookup"><span data-stu-id="30526-126">If the button is supposed to perform a task based on the values of other controls, those controls must have set the DT_SET_IMMEDIATE flag.</span></span> 
  
<span data-ttu-id="30526-127">Le **membre ulbLpszLabel** est la position dans la mémoire de la chaîne de caractères qui s’affiche sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="30526-127">The **ulbLpszLabel** member is the position in memory of the character string that is displayed on the button.</span></span> <span data-ttu-id="30526-128">Les fournisseurs de services peuvent ajouter un caractère « eter » () pour indiquer un accélérateur &amp; Windows dans l’étiquette du bouton.</span><span class="sxs-lookup"><span data-stu-id="30526-128">Service providers can add an ampersand character (&amp;) to indicate a Windows accelerator in the button label.</span></span> <span data-ttu-id="30526-129">Appuyer sur une touche d’accélérateur a le même effet que de cliquer sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="30526-129">Pressing an accelerator key has the same effect as clicking the button.</span></span> 
  
<span data-ttu-id="30526-130">Le **membre ulPRControl** décrit une propriété d’objet qui, lorsqu’elle est ouverte avec la méthode **IMAPIProp::OpenProperty,** renvoie un pointeur vers un objet de contrôle.</span><span class="sxs-lookup"><span data-stu-id="30526-130">The **ulPRControl** member describes an object property that, when opened with the **IMAPIProp::OpenProperty** method, returns a pointer to a control object.</span></span> <span data-ttu-id="30526-131">L’implémentation d’un objet de contrôle qui prend en charge l’interface **IMAPIControl** est un moyen d’étendre l’ensemble de fonctionnalités MAPI et de définir l’opération ou la tâche qui se produit lorsque l’utilisateur clique sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="30526-131">Implementing a control object that supports the **IMAPIControl** interface is a way to extend the MAPI feature set and define the operation or task that occurs when the button is clicked.</span></span> <span data-ttu-id="30526-132">**IMAPIControl fournit** deux méthodes de manipulation des boutons : [GetState](imapicontrol-getstate.md) pour désactiver ou activer les boutons et [Activate](imapicontrol-activate.md) pour gérer les clics de bouton.</span><span class="sxs-lookup"><span data-stu-id="30526-132">**IMAPIControl** supplies two methods for manipulating buttons: [GetState](imapicontrol-getstate.md) to disable or enable buttons and [Activate](imapicontrol-activate.md) to handle button clicks.</span></span> 
  
<span data-ttu-id="30526-133">Pour obtenir une vue d’ensemble des tableaux d’affichage, voir [Tableaux d’affichage.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="30526-133">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="30526-134">Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="30526-134">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="30526-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30526-135">See also</span></span>



[<span data-ttu-id="30526-136">DTCTL</span><span class="sxs-lookup"><span data-stu-id="30526-136">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="30526-137">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="30526-137">MAPI Structures</span></span>](mapi-structures.md)

