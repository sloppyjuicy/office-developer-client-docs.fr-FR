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
ms.openlocfilehash: 20831901567f177ada70a6cea94db0537786db94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571436"
---
# <a name="itabledatahrnotify"></a><span data-ttu-id="f1f73-103">ITableData::HrNotify</span><span class="sxs-lookup"><span data-stu-id="f1f73-103">ITableData::HrNotify</span></span>

  
  
<span data-ttu-id="f1f73-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1f73-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1f73-105">Envoie une notification pour une ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="f1f73-105">Sends a notification for a table row.</span></span>
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="f1f73-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="f1f73-106">Parameters</span></span>

 <span data-ttu-id="f1f73-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f1f73-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f1f73-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="f1f73-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f1f73-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="f1f73-109">_cValues_</span></span>
  
> <span data-ttu-id="f1f73-110">[in] Le nombre de valeurs de propriété dans la structure [SPropValue](spropvalue.md) indiqué par le paramètre _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="f1f73-110">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpSPropValue_ parameter.</span></span> 
    
 <span data-ttu-id="f1f73-111">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="f1f73-111">_lpSPropValue_</span></span>
  
> <span data-ttu-id="f1f73-112">[in] Pointeur vers une structure **SPropValue** qui décrit les valeurs des colonnes de la ligne cible.</span><span class="sxs-lookup"><span data-stu-id="f1f73-112">[in] A pointer to an **SPropValue** structure that describes the values of the columns in the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f1f73-113">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f1f73-113">Return value</span></span>

<span data-ttu-id="f1f73-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="f1f73-114">S_OK</span></span> 
  
> <span data-ttu-id="f1f73-115">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f1f73-115">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f1f73-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="f1f73-116">Remarks</span></span>

<span data-ttu-id="f1f73-117">La méthode **ITableData::HrNotify** envoie une notification TABLE_ROW_MODIFIED pour la ligne qui correspond à la ligne décrite par les propriétés désignées par le paramètre _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="f1f73-117">The **ITableData::HrNotify** method sends a TABLE_ROW_MODIFIED notification for the row that matches the row described by the properties pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="f1f73-118">**HrNotify** envoie la notification indépendamment si des modifications ont été effectuées à la ligne.</span><span class="sxs-lookup"><span data-stu-id="f1f73-118">**HrNotify** sends the notification regardless of whether changes have occurred to the row.</span></span> <span data-ttu-id="f1f73-119">Tous les clients et les fournisseurs de services qui ont des vues de la table et ont appelé [IMAPITable::Advise](imapitable-advise.md) pour inscrire les notifications sur leurs vues reçoivent cette notification.</span><span class="sxs-lookup"><span data-stu-id="f1f73-119">All clients and service providers that have views of the table and have called [IMAPITable::Advise](imapitable-advise.md) to register for notifications on their views receive this notification.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f1f73-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1f73-120">See also</span></span>



[<span data-ttu-id="f1f73-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f1f73-121">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="f1f73-122">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f1f73-122">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="f1f73-123">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f1f73-123">ITableData : IUnknown</span></span>](itabledataiunknown.md)

