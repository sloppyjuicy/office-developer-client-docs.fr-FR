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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 9e17e8ef7df33ffa248eec4195c00c77d0c49f94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587767"
---
# <a name="getattribimsgonistg"></a>GetAttribIMsgOnIStg

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Récupère les attributs de propriétés sur un objet [IMessage](imessageimapiprop.md) fournie par la fonction [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |IMessage.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de magasin d’applications clientes et message  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a>Paramètres

 _lpObject_
  
> [in] Pointeur vers un objet **IMessage** obtenu à partir de la fonction [OpenIMsgOnIStg](openimsgonistg.md) . 
    
 _lpPropTagArray_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété indiquant les propriétés dont les attributs doivent être récupérés. 
    
 _lppPropAttrArray_
  
> [out] Pointeur vers un pointeur vers la structure [SPropAttrArray](spropattrarray.md) retournée qui contient les attributs de la propriété extraite. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais une ou plusieurs propriétés ne sont pas accessible et ont été renvoyées avec un type de propriété de PT_ERROR.
    
## <a name="remarks"></a>Remarques

Attributs de la propriété est accessible uniquement sur propriété objets, autrement dit, l’implémentation de la [IMAPIProp : IUnknown](imapipropiunknown.md) interface. Pour rendre les propriétés MAPI disponible sur un objet de stockage structuré OLE, [OpenIMsgOnIStg](openimsgonistg.md) génère une [IMessage : IMAPIProp](imessageimapiprop.md) objet en haut de l’objet OLE **IStorage** . Les attributs de propriété sur de tels objets peuvent définir ou a été modifiés avec [SetAttribIMsgOnIStg](setattribimsgonistg.md) et récupérés par **GetAttribIMsgOnIStg**. 
  
> [!NOTE]
> **GetAttribIMsgOnIStg** et **SetAttribIMsgOnIStg** ne fonctionnent pas sur tous les objets **IMessage** . Ils ne sont valides pour **IMessage**- sur - objets **IStorage** renvoyés par **OpenIMsgOnIStg**. 
  
Le nombre et les positions des attributs dans le paramètre _lppPropAttrArray_ correspondent au nombre et les positions des balises de propriété dans le paramètre _lpPropTagArray_ . 
  

