---
title: ITableDataHrNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrNotify
api_type:
- COM
ms.assetid: 98548b50-342e-434a-9ad3-c37ba418c5ce
ms.openlocfilehash: 7c05b0c4dcef2f19466f09db81a2ff161fd2b93d
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379408"
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

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _cValues_
  
> [in] Nombre de valeurs de propriété dans la structure [SPropValue](spropvalue.md) pointée par  _le paramètre lpSPropValue_ . 
    
 _lpSPropValue_
  
> [in] Pointeur vers une structure **SPropValue** qui décrit les valeurs des colonnes de la ligne cible. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

La **méthode ITableData::HrNotify** envoie une notification TABLE_ROW_MODIFIED pour la ligne qui correspond à la ligne décrite par les propriétés pointées par le paramètre  _lpSPropValue_ . **HrNotify envoie** la notification, que des modifications soient apportées à la ligne ou non. Tous les clients et fournisseurs de services qui ont des vues de la table et qui ont appelé [IMAPITable::Advise](imapitable-advise.md) pour s’inscrire aux notifications sur leurs vues reçoivent cette notification. 
  
## <a name="see-also"></a>Voir aussi



[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

