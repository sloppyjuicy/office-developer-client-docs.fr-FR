---
title: ITableDataHrNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrNotify
api_type:
- COM
ms.assetid: 98548b50-342e-434a-9ad3-c37ba418c5ce
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: aa2170bf4bedfb441ad4808f774f6f71d5caf85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413268"
---
# <a name="itabledatahrnotify"></a><span data-ttu-id="f3fa6-103">ITableData::HrNotify</span><span class="sxs-lookup"><span data-stu-id="f3fa6-103">ITableData::HrNotify</span></span>

  
  
<span data-ttu-id="f3fa6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3fa6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3fa6-105">Envoie une notification pour une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="f3fa6-105">Sends a notification for a table row.</span></span>
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="f3fa6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f3fa6-106">Parameters</span></span>

 <span data-ttu-id="f3fa6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f3fa6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f3fa6-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="f3fa6-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f3fa6-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="f3fa6-109">_cValues_</span></span>
  
> <span data-ttu-id="f3fa6-110">[in] Nombre de valeurs de propriété dans la structure [SPropValue](spropvalue.md) pointée par _le paramètre lpSPropValue._</span><span class="sxs-lookup"><span data-stu-id="f3fa6-110">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpSPropValue_ parameter.</span></span> 
    
 <span data-ttu-id="f3fa6-111">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="f3fa6-111">_lpSPropValue_</span></span>
  
> <span data-ttu-id="f3fa6-112">[in] Pointeur vers une structure **SPropValue** qui décrit les valeurs des colonnes de la ligne cible.</span><span class="sxs-lookup"><span data-stu-id="f3fa6-112">[in] A pointer to an **SPropValue** structure that describes the values of the columns in the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f3fa6-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f3fa6-113">Return value</span></span>

<span data-ttu-id="f3fa6-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3fa6-114">S_OK</span></span> 
  
> <span data-ttu-id="f3fa6-115">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f3fa6-115">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3fa6-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="f3fa6-116">Remarks</span></span>

<span data-ttu-id="f3fa6-117">La **méthode ITableData::HrNotify** envoie une notification TABLE_ROW_MODIFIED pour la ligne qui correspond à la ligne décrite par les propriétés pointées par le paramètre _lpSPropValue._</span><span class="sxs-lookup"><span data-stu-id="f3fa6-117">The **ITableData::HrNotify** method sends a TABLE_ROW_MODIFIED notification for the row that matches the row described by the properties pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="f3fa6-118">**HrNotify envoie** la notification, que des modifications soient apportées à la ligne ou non.</span><span class="sxs-lookup"><span data-stu-id="f3fa6-118">**HrNotify** sends the notification regardless of whether changes have occurred to the row.</span></span> <span data-ttu-id="f3fa6-119">Tous les clients et fournisseurs de services qui ont des vues de la table et qui ont appelé [IMAPITable::Advise](imapitable-advise.md) pour s’inscrire aux notifications sur leurs vues reçoivent cette notification.</span><span class="sxs-lookup"><span data-stu-id="f3fa6-119">All clients and service providers that have views of the table and have called [IMAPITable::Advise](imapitable-advise.md) to register for notifications on their views receive this notification.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f3fa6-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3fa6-120">See also</span></span>



[<span data-ttu-id="f3fa6-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f3fa6-121">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="f3fa6-122">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f3fa6-122">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="f3fa6-123">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f3fa6-123">ITableData : IUnknown</span></span>](itabledataiunknown.md)

