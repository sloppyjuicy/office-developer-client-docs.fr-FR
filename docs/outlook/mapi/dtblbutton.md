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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e0797364eb4ec24793f64bad2f4d838507c236e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571065"
---
# <a name="dtblbutton"></a><span data-ttu-id="c8148-103">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="c8148-103">DTBLBUTTON</span></span>

  
  
<span data-ttu-id="c8148-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8148-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8148-105">Contient des informations sur un contrôle bouton pour une boîte de dialogue établi à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c8148-105">Contains information about a button control for a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8148-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c8148-106">Header file:</span></span>  <br/> |<span data-ttu-id="c8148-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8148-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c8148-108">Macro connexe :</span><span class="sxs-lookup"><span data-stu-id="c8148-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="c8148-109">SizedDtblButton</span><span class="sxs-lookup"><span data-stu-id="c8148-109">SizedDtblButton</span></span>](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a><span data-ttu-id="c8148-110">Members</span><span class="sxs-lookup"><span data-stu-id="c8148-110">Members</span></span>

 <span data-ttu-id="c8148-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="c8148-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="c8148-112">Position dans la mémoire de la chaîne de caractères qui s’affiche sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="c8148-112">Position in memory of the character string that is displayed on the button.</span></span>
    
 <span data-ttu-id="c8148-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c8148-113">**ulFlags**</span></span>
  
> <span data-ttu-id="c8148-114">Masque de bits d’indicateurs utilisés pour désigner le format de l’étiquette vers laquelle pointé le membre **ulbLpszLabel** .</span><span class="sxs-lookup"><span data-stu-id="c8148-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="c8148-115">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="c8148-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="c8148-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c8148-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c8148-117">L’étiquette est au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="c8148-117">The label is in Unicode format.</span></span> <span data-ttu-id="c8148-118">Si l’indicateur MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="c8148-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
 <span data-ttu-id="c8148-119">**ulPRControl**</span><span class="sxs-lookup"><span data-stu-id="c8148-119">**ulPRControl**</span></span>
  
> <span data-ttu-id="c8148-120">Balise de propriété pour une propriété de type PT_OBJECT qui implémente l’interface [IMAPIControl](imapicontroliunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="c8148-120">Property tag for a property of type PT_OBJECT that implements the [IMAPIControl](imapicontroliunknown.md) interface.</span></span> <span data-ttu-id="c8148-121">Lorsque le bouton est activé, MAPI appelle la méthode de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour la mise en œuvre de la table affichage [IMAPIProp](imapipropiunknown.md) d’extraire cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c8148-121">When the button is clicked, MAPI calls the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the display table's [IMAPIProp](imapipropiunknown.md) implementation to retrieve this property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c8148-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="c8148-122">Remarks</span></span>

<span data-ttu-id="c8148-123">Une structure **DTBLBUTTON** décrit un contrôle bouton qui, lorsque vous cliquez dessus, permet à un utilisateur commencer une opération.</span><span class="sxs-lookup"><span data-stu-id="c8148-123">A **DTBLBUTTON** structure describes a button a control that, when clicked, allows a user to begin an operation.</span></span> <span data-ttu-id="c8148-124">En règle générale, un bouton entraîne une boîte de dialogue modale s’affiche ou des tâches de programmation à appeler.</span><span class="sxs-lookup"><span data-stu-id="c8148-124">Typically, clicking a button causes a modal dialog box to be displayed or a programmatic task to be invoked.</span></span> <span data-ttu-id="c8148-125">Fournisseurs de service peuvent implémenter rien via un contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="c8148-125">Service providers can implement anything through a button control.</span></span> <span data-ttu-id="c8148-126">Si le bouton est supposé effectuer une tâche en fonction des valeurs d’autres contrôles, ces contrôles doivent avoir défini l’indicateur DT_SET_IMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="c8148-126">If the button is supposed to perform a task based on the values of other controls, those controls must have set the DT_SET_IMMEDIATE flag.</span></span> 
  
<span data-ttu-id="c8148-127">Le membre **ulbLpszLabel** est la position dans la mémoire de la chaîne de caractères qui s’affiche sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="c8148-127">The **ulbLpszLabel** member is the position in memory of the character string that is displayed on the button.</span></span> <span data-ttu-id="c8148-128">Fournisseurs de services peuvent ajouter une esperluette (&amp;) pour indiquer un raccourci Windows dans l’étiquette du bouton.</span><span class="sxs-lookup"><span data-stu-id="c8148-128">Service providers can add an ampersand character (&amp;) to indicate a Windows accelerator in the button label.</span></span> <span data-ttu-id="c8148-129">Appuyer sur une touche d’accès rapide a le même effet qu’un clic sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="c8148-129">Pressing an accelerator key has the same effect as clicking the button.</span></span> 
  
<span data-ttu-id="c8148-130">Le membre **ulPRControl** décrit une propriété d’objet qui, lorsque ouvert avec la méthode **IMAPIProp::OpenProperty** , retourne un pointeur vers un objet control.</span><span class="sxs-lookup"><span data-stu-id="c8148-130">The **ulPRControl** member describes an object property that, when opened with the **IMAPIProp::OpenProperty** method, returns a pointer to a control object.</span></span> <span data-ttu-id="c8148-131">Implémentation d’un objet de contrôle qui prend en charge l’interface **IMAPIControl** consiste à étendre le jeu de fonctions MAPI et définir l’opération ou la tâche qui se produit lorsque l’utilisateur clique sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="c8148-131">Implementing a control object that supports the **IMAPIControl** interface is a way to extend the MAPI feature set and define the operation or task that occurs when the button is clicked.</span></span> <span data-ttu-id="c8148-132">**IMAPIControl** fournit deux méthodes pour la manipulation des boutons : [GetState](imapicontrol-getstate.md) pour désactiver ou activer les boutons et [Activer](imapicontrol-activate.md) pour gérer les clics de bouton.</span><span class="sxs-lookup"><span data-stu-id="c8148-132">**IMAPIControl** supplies two methods for manipulating buttons: [GetState](imapicontrol-getstate.md) to disable or enable buttons and [Activate](imapicontrol-activate.md) to handle button clicks.</span></span> 
  
<span data-ttu-id="c8148-133">Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c8148-133">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="c8148-134">Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="c8148-134">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c8148-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8148-135">See also</span></span>



[<span data-ttu-id="c8148-136">DTCTL</span><span class="sxs-lookup"><span data-stu-id="c8148-136">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="c8148-137">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="c8148-137">MAPI Structures</span></span>](mapi-structures.md)

