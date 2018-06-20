---
title: IMAPIControlActivate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.Activate
api_type:
- COM
ms.assetid: 2b641030-2429-4217-a648-0a9f3d1a1b29
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: fb6cd23acdb81af250e7e6dfe6facf7226850363
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783692"
---
# <a name="imapicontrolactivate"></a><span data-ttu-id="e94e8-103">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="e94e8-103">IMAPIControl::Activate</span></span>

  
  
<span data-ttu-id="e94e8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e94e8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e94e8-105">Effectue une tâche telle que l’affichage d’une boîte de dialogue ou le démarrage d’une opération de programmation lorsqu’un utilisateur de l’application client clique sur le contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="e94e8-105">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a><span data-ttu-id="e94e8-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="e94e8-106">Parameters</span></span>

 <span data-ttu-id="e94e8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e94e8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e94e8-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="e94e8-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="e94e8-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e94e8-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="e94e8-110">[in] Handle vers la fenêtre parente de la boîte de dialogue sur lequel apparaît le contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="e94e8-110">[in] A handle to the parent window of the dialog box on which the button control appears.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e94e8-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e94e8-111">Return value</span></span>

<span data-ttu-id="e94e8-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="e94e8-112">S_OK</span></span> 
  
> <span data-ttu-id="e94e8-113">Le contrôle bouton a été activé avec succès.</span><span class="sxs-lookup"><span data-stu-id="e94e8-113">The button control was successfully activated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e94e8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e94e8-114">Remarks</span></span>

<span data-ttu-id="e94e8-115">La méthode **IMAPIControl::Activate** effectue des tâches suivant un bouton du contrôle bouton.</span><span class="sxs-lookup"><span data-stu-id="e94e8-115">The **IMAPIControl::Activate** method performs tasks following a user's click of the button control.</span></span> <span data-ttu-id="e94e8-116">Une fois que le clic se produit dans le cadre du traitement de la table d’affichage, MAPI effectue un appel à **Activer** après le premier appel [IMAPIControl::GetState](imapicontrol-getstate.md) pour déterminer si le bouton est activé.</span><span class="sxs-lookup"><span data-stu-id="e94e8-116">After the click occurs, as part of the processing of the display table, MAPI makes a call to **Activate** after first calling [IMAPIControl::GetState](imapicontrol-getstate.md) to determine whether the button is enabled.</span></span> 
  
<span data-ttu-id="e94e8-117">Pour plus d’informations sur la façon d’implémenter **Activate** et l’autre [IMAPIControl : IUnknown](imapicontroliunknown.md) méthodes, voir [Implémentation d’objet de contrôle](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="e94e8-117">For more information about how to implement **Activate** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e94e8-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e94e8-118">See also</span></span>



[<span data-ttu-id="e94e8-119">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="e94e8-119">IMAPIControl::GetState</span></span>](imapicontrol-getstate.md)
  
[<span data-ttu-id="e94e8-120">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e94e8-120">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

