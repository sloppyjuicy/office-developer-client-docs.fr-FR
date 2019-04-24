---
title: GetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: bb27b28a-b2bd-4d4a-b0bb-0692f3de8e16
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 16e85eabc067bd82f5fb89c917afaf2831c75673
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300468"
---
# <a name="getattribimsgonistg"></a>GetAttribIMsgOnIStg

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère les attributs des propriétés sur un objet [IMessage](imessageimapiprop.md) fourni par la fonction [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |IMessage. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de banques de messages  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a>Paramètres

 _lpObject_
  
> dans Pointeur vers un objet **IMessage** obtenu à partir de la fonction [OpenIMsgOnIStg](openimsgonistg.md) . 
    
 _lpPropTagArray_
  
> dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété indiquant les propriétés pour lesquelles les attributs doivent être récupérés. 
    
 _lppPropAttrArray_
  
> remarquer Pointeur vers un pointeur vers la structure [SPropAttrArray](spropattrarray.md) renvoyée qui contient les attributs de propriété récupérés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_W_ERRORS_RETURNED 
  
> L'appel a réussi globalement, mais une ou plusieurs propriétés n'ont pas été accessibles et ont été renvoyées avec un type de propriété PT_ERROR.
    
## <a name="remarks"></a>Remarques

Les attributs de propriété ne sont accessibles que sur les objets Property, c'est-à-dire les objets qui implémentent l'interface [IMAPIProp: IUnknown](imapipropiunknown.md) . Pour que les propriétés MAPI soient disponibles sur un objet de stockage structuré OLE, [OpenIMsgOnIStg](openimsgonistg.md) crée un objet [IMessage: IMAPIProp](imessageimapiprop.md) en haut de l'objet OLE **IStorage** . Les attributs de propriété sur ces objets peuvent être définis ou modifiés avec [SetAttribIMsgOnIStg](setattribimsgonistg.md) et récupérés avec **GetAttribIMsgOnIStg**. 
  
> [!NOTE]
> **GetAttribIMsgOnIStg** et **SetAttribIMsgOnIStg** ne fonctionnent pas sur tous les objets **IMessage** . Elles ne sont valides que pour les objets **IMessage**sur le **IStorage** renvoyés par **OpenIMsgOnIStg**. 
  
Le nombre et les positions des attributs dans le paramètre _lppPropAttrArray_ correspondent au nombre et aux positions des balises de propriété dans le paramètre _lpPropTagArray_ . 
  

