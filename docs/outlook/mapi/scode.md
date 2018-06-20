---
title: SCODE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: 2348cce1-07c3-49ed-ae03-79e477d3c6c2
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6cd9dfe8fabd1ae7a4389550c628fb7ceff09ea8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787073"
---
# <a name="scode"></a>SCODE

**S’applique à**: Outlook 
  
Une valeur d’état de 32 bits qui est utilisée pour décrire une erreur ou un avertissement. 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a>Remarques

Le type de données **SCODE** est la même que le type de données [HRESULT](hresult.md) . 
  
Une valeur **SCODE** est divisée en quatre champs : 
  
- Un code de gravité bits unique qui est défini sur 0 pour indiquer la réussite et 1 pour indiquer l’échec.
    
- Un champ réservé 11 bits
    
- Un code de fonction 4 bits qui indique la zone responsable de l’erreur ou avertissement.
    
- Une erreur de 16 bits ou un code d’avertissement qui décrit le problème qui est à l’origine de l’erreur ou avertissement.
    
La plupart des méthodes et fonctions MAPI renvoient des valeurs **SCODE** définis en tant que types de données **HRESULT** comme les fonctions et méthodes OLE. OLE définit plusieurs macros qui peuvent être utilisés pour convertir les **SCODE** un **HRESULT**.
  
> [!NOTE]
> 64 bits, MAPI, **SCODE** est toujours une valeur 32 bits. 
  
Pour plus d’informations sur l’utilisation de MAPI sur le type de données **SCODE** , voir [Gestion des erreurs](error-handling-in-mapi.md). Pour plus d’informations sur OLE et le type de données **SCODE** , voir la *référence du programmeur OLE* . 
  
## <a name="see-also"></a>Voir aussi



[[HRESULT]](hresult.md)


[Types de donn�es MAPI](mapi-data-types.md)

