---
title: IMAPITableQueryPosition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryPosition
api_type:
- COM
ms.assetid: 510b2e21-ba27-47dd-87cb-2a549e31fa28
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 502bc24ece37c91e2cac23cf8486df96d5a71377
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584337"
---
# <a name="imapitablequeryposition"></a>IMAPITable::QueryPosition

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Extrait la position de ligne de tableau en cours du curseur, basée sur une valeur décimale.
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a>Paramètres

 _lpulRow_
  
> [out] Pointeur vers le nombre de la ligne active. Numéro de ligne est zéro ; la première ligne dans le tableau est égale à zéro. 
    
 _lpulNumerator_
  
> [out] Pointeur vers le numérateur pour la fraction qui identifie la position de la table.
    
 _lpulDenominator_
  
> [out] Pointeur vers le dénominateur de la fraction qui identifie la position de la table. Le paramètre _lpulDenominator_ ne peut pas être égal à zéro. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La méthode a renvoyé les valeurs valides dans _lpulRow_, _lpulNumerator_et _lpulDenominator_.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::QueryPosition** détermine la position de ligne en cours et renvoie le nombre de la ligne active et une valeur décimale qui indique sa position relative à la fin de la table. MAPI définit la ligne active en tant que la ligne suivante à lire. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Vous n’avez pas besoin renvoyer le nombre exact de lignes dans la table pour le paramètre _lpulDenominator_ ; Il peut être une estimation. 
  
Si vous ne pouvez pas déterminer la ligne actuelle, retourne une valeur de 0xFFFFFFFF _lpulRow_.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez utiliser **QueryPosition** pour positionner un curseur de défilement dans une barre de défilement. Par exemple, dans une table contenant les 100 lignes, si **QueryPosition** renvoie la valeur 75 dans le paramètre _lpulNumerator_ , 100 dans le paramètre _lpulDenominator_ et 75 dans le paramètre _lpulRow_ , vous pouvez placer le défilement case 3/4 la méthode dans la barre de défilement. 
  
Ne vous fiez pas la valeur de _lpulDenominator_ est le nombre de lignes dans le tableau. **QueryPosition** ne peut pas toujours identifier le curseur est positionné sur la ligne exacte. 
  
Un appel à **QueryPosition** peut impliquer des grandes quantités de mémoire, en particulier pour les grandes tables par catégorie. Si le paramètre _lpulRow_ est défini sur 0xFFFFFFFF, trop de mémoire était nécessaire pour **QueryPosition** déterminer la ligne active. Appelez la méthode [IMAPI::SeekRowApprox](imapitable-seekrowapprox.md) pour positionner la table à la ligne identifiée par les paramètres _lpulNumerator_ et _lpulDenominator_ . Toutefois, pas toujours attendez-vous **SeekRowApprox** pour établir que la position actuelle de la même ligne **que QueryPosition** aurait si la mémoire n’a pas été un facteur. 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

