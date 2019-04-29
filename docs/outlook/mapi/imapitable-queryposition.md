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
ms.openlocfilehash: 2e44d824bbb5cc96c51d7ca91eb639001bc52a71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415662"
---
# <a name="imapitablequeryposition"></a>IMAPITable::QueryPosition

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère la position de ligne de tableau actuelle du curseur, en fonction d'une valeur fractionnaire.
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a>Paramètres

 _lpulRow_
  
> remarquer Pointeur vers le numéro de la ligne actuelle. Le numéro de ligne est de base zéro; la première ligne du tableau est égale à zéro. 
    
 _lpulNumerator_
  
> remarquer Pointeur vers le numérateur de la fraction identifiant la position du tableau.
    
 _lpulDenominator_
  
> remarquer Pointeur vers le dénominateur de la fraction identifiant la position de la table. Le paramètre _lpulDenominator_ ne peut pas être égal à zéro. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La méthode a renvoyé des valeurs valides dans _lpulRow_, _lpulNumerator_et _lpulDenominator_.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable:: QueryPosition** détermine la position de ligne active et renvoie à la fois le numéro de la ligne active et une valeur fractionnaire indiquant sa position relative à la fin de la table. MAPI définit la ligne actuelle en tant que ligne suivante à lire. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Vous n'avez pas besoin de renvoyer le nombre exact de lignes dans le tableau pour le paramètre _lpulDenominator_ ; Il peut s'agir d'une approximation. 
  
Si vous ne parvenez pas à déterminer la ligne active, renvoyez une valeur de 0xFFFFFFFF dans _lpulRow_.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser **QueryPosition** pour positionner une case de défilement dans une barre de défilement. Par exemple, dans une table contenant 100 lignes, si **QueryPosition** renvoie la valeur 75 dans le paramètre _lpulNumerator_ , 100 dans le paramètre _lpulDenominator_ et 75 dans le paramètre _lpulRow_ , vous pouvez placer le curseur de défilement 3/4 de la barre de défilement. 
  
Ne comptez pas sur la valeur de _lpulDenominator_ en tant que nombre de lignes dans le tableau. **QueryPosition** ne peut pas toujours identifier la ligne exacte sur laquelle le curseur est positionné. 
  
Un appel à **QueryPosition** peut impliquer de grandes quantités de mémoire, en particulier pour les grandes tables classées. Si le paramètre _lpulRow_ est défini sur 0xFFFFFFFF, trop de mémoire a été requise pour **QueryPosition** pour déterminer la ligne actuelle. Appelez la méthode [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) pour positionner la table sur la ligne identifiée par les paramètres _lpulNumerator_ et _lpulDenominator_ . Toutefois, ne s'attend pas toujours à ce que **SeekRowApprox** établisse comme position actuelle, la même ligne que **QueryPosition** aurait si la mémoire n'avait pas été un facteur. 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

