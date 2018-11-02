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
# <a name="itabledatahrnotify"></a>ITableData::HrNotify

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Envoie une notification pour une ligne de tableau.
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _cValues_
  
> [in] Le nombre de valeurs de propriété dans la structure [SPropValue](spropvalue.md) indiqué par le paramètre _lpSPropValue_ . 
    
 _lpSPropValue_
  
> [in] Pointeur vers une structure **SPropValue** qui décrit les valeurs des colonnes de la ligne cible. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

La méthode **ITableData::HrNotify** envoie une notification TABLE_ROW_MODIFIED pour la ligne qui correspond à la ligne décrite par les propriétés désignées par le paramètre _lpSPropValue_ . **HrNotify** envoie la notification indépendamment si des modifications ont été effectuées à la ligne. Tous les clients et les fournisseurs de services qui ont des vues de la table et ont appelé [IMAPITable::Advise](imapitable-advise.md) pour inscrire les notifications sur leurs vues reçoivent cette notification. 
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

