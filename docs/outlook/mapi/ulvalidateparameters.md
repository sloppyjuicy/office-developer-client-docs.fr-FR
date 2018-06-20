---
title: UlValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParameters
api_type:
- COM
ms.assetid: fb9050c9-5797-44f0-8bf5-6264f4e6d7c3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 42b2f8e9695b1dbdc5ea02db5a4e8a0eaba6099c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787423"
---
# <a name="ulvalidateparameters"></a>UlValidateParameters

  
  
**S’applique à**: Outlook 
  
Appelle une fonction interne pour vérifier que les applications clientes de paramètres transmis à MAPI et les fournisseurs de services. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
HRESULT UlValidateParameters(
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
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs. 
    
MAPI_E_CALL_FAILED 
  
> Une erreur d’origine inattendu ou inconnu a empêché l’opération de se terminer.
    
## <a name="remarks"></a>Remarques

La macro **UlValidateParameters** a été remplacée par la macro [UlValidateParms](ulvalidateparms.md) . **UlValidateParameters** ne fonctionne pas correctement sur les plateformes RISC et est maintenant interdit la compilation sur les. Il compile et fonctionne correctement sur les plateformes Intel, mais **UlValidateParms** est recommandé sur toutes les plateformes. 
  

