---
title: Utilisation de la mémoire et des tables
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: afd69f5a3fff69f670d6be78ba4957307cdb6995
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436859"
---
# <a name="tables-and-memory-usage"></a>Utilisation de la mémoire et des tables

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un problème important lié à la récupération des données d’une table est l’utilisation de la mémoire. Le manque de mémoire disponible peut entraîner l’échec [d’IMAPITable::QueryRows](imapitable-queryrows.md) et [HrQueryAllRows,](hrqueryallrows.md) en renvoyant moins de lignes que le nombre souhaité. Le choix de la méthode ou de la fonction à utiliser pour récupérer les données d’un tableau varie selon que la table doit tenir dans la mémoire et, si elle ne l’est pas, si l’échec est acceptable. 
  
Étant donné qu’il n’est pas toujours facile de déterminer la quantité de données qui s’intégrera dans la mémoire à la fois, MAPI fournit des instructions de base pour qu’une application cliente ou un fournisseur de services suive. N’oubliez pas qu’il existe toujours des exceptions, en fonction de l’implémentation de la table particulière et de la façon dont les données sous-jacentes sont stockées.
  
Les instructions suivantes peuvent être utilisées pour évaluer l’utilisation de la mémoire des tableaux :
  
- Les clients qui peuvent tolérer un travail occasionnel définissent l’utilisation de la mémoire dans la plage de mégaoctets et peuvent supposer qu’ils n’auront aucun problème à lire un tableau entier en mémoire. 
    
- Les restrictions ont une incidence sur l’utilisation de la mémoire par une table. Une table très restreinte avec un grand nombre de lignes, telles qu’une table des matières, peut être attendue pour tenir dans la mémoire, alors qu’une grande table non restreinte ne le peut généralement pas. 
    
- Plusieurs tables de MAPI, telles que les tables d’état, de profil, de service de message, de fournisseur et de magasin de messages, sont généralement stockées en mémoire. Il s’agit généralement de petites tables. Toutefois, il existe des exceptions. Par exemple, un fournisseur de profils basé sur un serveur peut générer une table de profils plus grande qui ne pourra pas tenir.
    
Pour récupérer toutes les lignes d’un tableau qui s’intègrera dans la mémoire sans problème, appelez [HrQueryAllRows](hrqueryallrows.md), en fixant le nombre maximal de lignes sur zéro.
  
Pour récupérer toutes les lignes d’un tableau qui peuvent ou non tenir dans la mémoire, générant une erreur, appelez **HrQueryAllRows** en spécifiant un nombre maximal de lignes. Le nombre maximal de lignes doit être supérieur au nombre minimal de lignes nécessaires. Si un client doit accéder à au moins 50 lignes à partir d’un tableau de 300 lignes, le nombre maximal de lignes doit être d’au moins 51. 
  
Pour récupérer toutes les lignes d’un tableau qui n’est pas censé tenir dans la mémoire, appelez [IMAPITable::QueryRows](imapitable-queryrows.md) dans une boucle avec un nombre de lignes relativement faible, comme l’illustre l’exemple de code suivant : 
  
```cpp
HRESULT     hr;
LPSRowSet   pRows = NULL;
LONG        irow;
LONG            cAsk = 50;                  // adjust this value
while ((hr = pTable->QueryRows(cAsk, 0, &pRows)) == hrSuccess
        && pRows->cRows != 0)
{
    for (irow = 0; irow < prows->cRows; ++irow)
    {
        // process the row...
    }
    FreeProws(pRows);
    pRows = NULL;
}
if (hr)
{
    // handle the error...
}
 
```

Lorsque cette boucle est terminée et que toutes les lignes du tableau ont été traitées et  _que cRows_ est zéro, la position du curseur est généralement en bas du tableau. 
  
## <a name="see-also"></a>Voir aussi

- [MAPI Tables](mapi-tables.md)

