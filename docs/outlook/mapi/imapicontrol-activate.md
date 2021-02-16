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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d3b47e423daf428c67761d13deef1ae0858c91c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418014"
---
# <a name="imapicontrolactivate"></a><span data-ttu-id="9fae4-103">IMAPIControl::Activate</span><span class="sxs-lookup"><span data-stu-id="9fae4-103">IMAPIControl::Activate</span></span>

  
  
<span data-ttu-id="9fae4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fae4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fae4-105">Effectue une tâche telle que l’affichage d’une boîte de dialogue ou le démarrage d’une opération par programme lorsqu’un utilisateur de l’application cliente clique sur le contrôle de bouton.</span><span class="sxs-lookup"><span data-stu-id="9fae4-105">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a><span data-ttu-id="9fae4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9fae4-106">Parameters</span></span>

 <span data-ttu-id="9fae4-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9fae4-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9fae4-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="9fae4-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9fae4-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9fae4-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="9fae4-110">[in] Poignée vers la fenêtre parente de la boîte de dialogue sur laquelle le contrôle de bouton apparaît.</span><span class="sxs-lookup"><span data-stu-id="9fae4-110">[in] A handle to the parent window of the dialog box on which the button control appears.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9fae4-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9fae4-111">Return value</span></span>

<span data-ttu-id="9fae4-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="9fae4-112">S_OK</span></span> 
  
> <span data-ttu-id="9fae4-113">Le contrôle de bouton a été activé avec succès.</span><span class="sxs-lookup"><span data-stu-id="9fae4-113">The button control was successfully activated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9fae4-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9fae4-114">Remarks</span></span>

<span data-ttu-id="9fae4-115">La **méthode IMAPIControl::Activate** effectue des tâches à la suite du clic d’un utilisateur sur le contrôle de bouton.</span><span class="sxs-lookup"><span data-stu-id="9fae4-115">The **IMAPIControl::Activate** method performs tasks following a user's click of the button control.</span></span> <span data-ttu-id="9fae4-116">Une fois que le clic s’est produit, dans le cadre du traitement de la table d’affichage, MAPI appelle **Activate** après avoir appelé [IMAPIControl::GetState](imapicontrol-getstate.md) pour déterminer si le bouton est activé.</span><span class="sxs-lookup"><span data-stu-id="9fae4-116">After the click occurs, as part of the processing of the display table, MAPI makes a call to **Activate** after first calling [IMAPIControl::GetState](imapicontrol-getstate.md) to determine whether the button is enabled.</span></span> 
  
<span data-ttu-id="9fae4-117">Pour plus d’informations sur l’implémentation **d’Activate** et des autres méthodes [IMAPIControl : IUnknown,](imapicontroliunknown.md) voir [Control Object Implementation](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="9fae4-117">For more information about how to implement **Activate** and the other [IMAPIControl : IUnknown](imapicontroliunknown.md) methods, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9fae4-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fae4-118">See also</span></span>



[<span data-ttu-id="9fae4-119">IMAPIControl::GetState</span><span class="sxs-lookup"><span data-stu-id="9fae4-119">IMAPIControl::GetState</span></span>](imapicontrol-getstate.md)
  
[<span data-ttu-id="9fae4-120">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9fae4-120">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

