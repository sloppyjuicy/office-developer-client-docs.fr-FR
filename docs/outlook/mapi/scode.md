---
title: SCODE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: 2348cce1-07c3-49ed-ae03-79e477d3c6c2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 781d0a0485740f5f13175307a5d5c6939d7d71fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586760"
---
# <a name="scode"></a>SCODE

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valeur d’état 32 bits utilisée pour décrire une erreur ou un avertissement. 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a>Remarques

Le type de données **SCODE** est identique au type de données [HRESULT.](hresult.md) 
  
Une **valeur SCODE** est divisée en quatre champs : 
  
- Code de gravité à bit unique qui est définie sur 0 pour indiquer la réussite et 1 pour indiquer l’échec.
    
- Champ réservé 11 bits
    
- Code de la facilité 4 bits qui indique la zone responsable de l’erreur ou de l’avertissement.
    
- Erreur 16 bits ou code d’avertissement qui décrit le problème à l’origine de l’erreur ou de l’avertissement.
    
De nombreuses fonctions et méthodes MAPI retournent des valeurs **SCODE** définies en tant que types de données **HRESULT,** tout comme les méthodes et fonctions OLE. OLE définit plusieurs macros qui peuvent être utilisées pour convertir entre **un SCODE** et un **HRESULT**.
  
> [!NOTE]
> Dans MAPI 64 bits, **SCODE** est toujours une valeur 32 bits. 
  
Pour plus d’informations sur la façon dont MAPI utilise le type de données **SCODE,** voir [Gestion des erreurs.](error-handling-in-mapi.md) Pour plus d’informations sur OLE et le type de données **SCODE,** voir  *OLE Programmer’s Reference*  . 
  
## <a name="see-also"></a>Voir aussi



[[HRESULT]](hresult.md)


[Types de données MAPI](mapi-data-types.md)

