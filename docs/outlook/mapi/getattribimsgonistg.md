---
title: GetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.GetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: bb27b28a-b2bd-4d4a-b0bb-0692f3de8e16
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f8e928ad0baed850adcb05c481c5c322048ed6c6
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63782838"
---
# <a name="getattribimsgonistg"></a>GetAttribIMsgOnIStg

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère les attributs des propriétés d’un objet [IMessage](imessageimapiprop.md) fourni par la [fonction OpenIMsgOnIStg](openimsgonistg.md) . 
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Imessage.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de magasins de messages  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a>Paramètres

 _lpObject_
  
> [in] Pointeur vers un **objet IMessage** obtenu à partir de la [fonction OpenIMsgOnIStg](openimsgonistg.md) . 
    
 _lpPropTagArray_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété indiquant les propriétés pour lesquelles les attributs doivent être récupérés. 
    
 _lppPropAttrArray_
  
> [out] Pointeur vers un pointeur vers la structure [SPropAttrArray](spropattrarray.md) renvoyée qui contient les attributs de propriété récupérés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi globalement, mais une ou plusieurs propriétés n’ont pas pu être accessibles et ont été renvoyées avec un type de propriété PT_ERROR.
    
## <a name="remarks"></a>Remarques

Les attributs de propriété sont accessibles uniquement sur les objets de propriété, c’est-à-dire les objets implémentant l’interface [IMAPIProp : IUnknown](imapipropiunknown.md) . Pour rendre les propriétés MAPI disponibles sur un objet de stockage structuré OLE, [OpenIMsgOnIStg](openimsgonistg.md) crée un objet [IMessage : IMAPIProp](imessageimapiprop.md) au-dessus de l’objet OLE **IStorage** . Les attributs de propriété de ces objets peuvent être définies ou modifiées avec [SetAttribIMsgOnIStg](setattribimsgonistg.md) et récupérées avec **GetAttribIMsgOnIStg**. 
  
> [!NOTE]
> **GetAttribIMsgOnIStg** et **SetAttribIMsgOnIStg** ne fonctionnent pas sur tous **les objets IMessage** . Elles ne sont valides que pour les objets IMessage-on-IStorage renvoyés par **OpenIMsgOnIStg**. 
  
Le nombre et les positions des attributs dans le paramètre _lppPropAttrArray_ correspondent au nombre et aux positions des balises de propriété dans le paramètre _lpPropTagArray_ . 
  

