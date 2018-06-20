---
title: ValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParameters
api_type:
- COM
ms.assetid: 80aadd11-5409-4636-8fad-fa2206336671
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 921417d8fc73ca9c1f126b2cb0add23f6625e3f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787462"
---
# <a name="validateparameters"></a>ValidateParameters

  
  
**S’applique à**: Outlook 
  
Appelle une fonction interne pour vérifier que les applications clientes de paramètres transmis à des fournisseurs de services. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Paramètres

 _eMethod_
  
> [in] Spécifie, par l’énumération, la méthode à valider. 
    
 _Premier_
  
> [in] Pointeur vers le premier argument dans la pile.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Tous les paramètres sont valides. 
    
MAPI_E_CALL_FAILED 
  
> Un ou plusieurs des paramètres ne sont pas valides.
    
## <a name="remarks"></a>Remarques

La macro **ValidateParameters** a été remplacée par la macro [ValidateParms](validateparms.md) . **ValidateParameters** ne fonctionne pas correctement sur les plateformes RISC et est maintenant interdit la compilation sur les. Il compile et fonctionne correctement sur les plateformes Intel, mais **ValidateParms** est recommandé sur toutes les plateformes. 
  

