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
# <a name="itabledatahrnotify"></a><span data-ttu-id="d557c-103">ITableData::HrNotify</span><span class="sxs-lookup"><span data-stu-id="d557c-103">ITableData::HrNotify</span></span>

  
  
<span data-ttu-id="d557c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d557c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d557c-105">Envoie une notification pour une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="d557c-105">Sends a notification for a table row.</span></span>
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="d557c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d557c-106">Parameters</span></span>

 <span data-ttu-id="d557c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d557c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d557c-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="d557c-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d557c-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="d557c-109">_cValues_</span></span>
  
> <span data-ttu-id="d557c-110">dans Nombre de valeurs de propriété dans la structure [SPropValue](spropvalue.md) vers laquelle pointe le paramètre _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="d557c-110">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpSPropValue_ parameter.</span></span> 
    
 <span data-ttu-id="d557c-111">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="d557c-111">_lpSPropValue_</span></span>
  
> <span data-ttu-id="d557c-112">dans Pointeur vers une structure **SPropValue** qui décrit les valeurs des colonnes dans la ligne cible.</span><span class="sxs-lookup"><span data-stu-id="d557c-112">[in] A pointer to an **SPropValue** structure that describes the values of the columns in the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d557c-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d557c-113">Return value</span></span>

<span data-ttu-id="d557c-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="d557c-114">S_OK</span></span> 
  
> <span data-ttu-id="d557c-115">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="d557c-115">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d557c-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="d557c-116">Remarks</span></span>

<span data-ttu-id="d557c-117">La méthode **ITableData:: HrNotify** envoie une notification TABLE_ROW_MODIFIED pour la ligne qui correspond à la ligne décrite par le paramètre _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="d557c-117">The **ITableData::HrNotify** method sends a TABLE_ROW_MODIFIED notification for the row that matches the row described by the properties pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="d557c-118">**HrNotify** envoie la notification, que les modifications aient ou non été apportées à la ligne.</span><span class="sxs-lookup"><span data-stu-id="d557c-118">**HrNotify** sends the notification regardless of whether changes have occurred to the row.</span></span> <span data-ttu-id="d557c-119">Tous les clients et fournisseurs de services qui ont des vues de la table et qui ont appelé la méthode [IMAPITable:: conseille](imapitable-advise.md) de s'inscrire aux notifications sur leurs vues recevez cette notification.</span><span class="sxs-lookup"><span data-stu-id="d557c-119">All clients and service providers that have views of the table and have called [IMAPITable::Advise](imapitable-advise.md) to register for notifications on their views receive this notification.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d557c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d557c-120">See also</span></span>



[<span data-ttu-id="d557c-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d557c-121">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="d557c-122">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d557c-122">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="d557c-123">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d557c-123">ITableData : IUnknown</span></span>](itabledataiunknown.md)

