---
title: SetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: 683d0d00-1b93-445d-86ff-180a3e6d2323
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 852ce31ba5ab02ff8f05dee25c9b32acb73130ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428829"
---
# <a name="setattribimsgonistg"></a>SetAttribIMsgOnIStg

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit ou modifie les attributs des propriétés d’un objet [IMessage](imessageimapiprop.md) fourni par la fonction [OpenIMsgOnIStg.](openimsgonistg.md) 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Imessage.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de magasins de messages  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a>Parameters

 _lpObject_
  
> [in] Pointeur vers l’objet pour lequel les attributs de propriété sont définies. 
    
 _lpPropTags_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) contenant un tableau de balises de propriété indiquant les propriétés pour lesquelles les attributs de propriété sont définies. 
    
 _lpPropAttrs_
  
> [in] Pointeur vers une structure [SPropAttrArray](spropattrarray.md) répertoriant les attributs de propriété à définir. 
    
 _lppPropProblems_
  
> [out] Pointeur vers la structure [SPropProblemArray](spropproblemarray.md) renvoyée contenant un ensemble de problèmes de propriété. Cette structure identifie les problèmes rencontrés si **SetAttribIMsgOnIStg** a pu définir certaines propriétés, mais pas toutes. Si un pointeur vers NULL est transmis dans le paramètre  _lppPropProblems,_ aucun tableau de problèmes de propriété n’est renvoyé, même si certaines propriétés n’ont pas été définies. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi globalement, mais une ou plusieurs propriétés n’ont pas pu être accessibles et ont été renvoyées avec un type de propriété PT_ERROR.
    
## <a name="remarks"></a>Remarques

Les attributs de propriété sont accessibles uniquement sur les objets de propriété, c’est-à-dire les objets implémentant l’interface [IMAPIProp : IUnknown.](imapipropiunknown.md) Pour rendre les propriétés MAPI disponibles sur un objet de stockage structuré OLE, [OpenIMsgOnIStg](openimsgonistg.md) crée un objet [IMessage : IMAPIProp](imessageimapiprop.md) au-dessus de l’objet **OLE IStorage.** Les attributs de propriété sur ces objets peuvent être définies ou modifiées avec **SetAttribIMsgOnIStg** et récupérées avec [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
 **Remarque** **: GetAttribIMsgOnIStg** et **SetAttribIMsgOnIStg** ne fonctionnent pas sur tous les objets **IMessage.** Ils sont uniquement valides pour les objets **IMessage**-on- **IStorage** renvoyés par **OpenIMsgOnIStg**. 
  
Dans le _paramètre lpPropAttrs,_ le numéro et la position des attributs doivent correspondre au numéro et à la position des balises de propriété transmises dans le paramètre _lpPropTags._ 
  
La **fonction SetAttribIMsgOnIStg** permet de rendre les propriétés de message en lecture seule lorsqu’elles sont requises par le **schéma IMessage.** L’exemple de fournisseur de magasins de messages l’utilise à cet effet. Pour plus d’informations, voir [Messages](mapi-messages.md). 
  

