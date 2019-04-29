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
  
Un problème important lié à la récupération des données d'une table est l'utilisation de la mémoire. L'absence de mémoire disponible peut entraîner l'échec d'une erreur [IMAPITable:: QueryRows](imapitable-queryrows.md) et [HrQueryAllRows](hrqueryallrows.md) , ce qui renvoie moins de lignes que le nombre souhaité. Le choix de la méthode ou de la fonction à utiliser pour récupérer les données de tableau dépend du fait que la table peut être ajustée en mémoire et, si elle ne l'est pas, si la défaillance est acceptable. 
  
Étant donné qu'il n'est pas toujours facile de déterminer la quantité de données pouvant être insérées dans la mémoire, MAPI fournit quelques instructions de base pour qu'une application client ou un fournisseur de services soit suivi. N'oubliez pas qu'il existe toujours des exceptions, en fonction de l'implémentation de table particulière et de la façon dont les données sous-jacentes sont stockées.
  
Les instructions suivantes peuvent être utilisées pour évaluer l'utilisation de la mémoire des tableaux:
  
- Les clients qui peuvent tolérer une utilisation occasionnelle de la mémoire du jeu de travail dans la plage de mégaoctets et peuvent supposer qu'ils n'auront aucun problème à lire une table entière dans la mémoire. 
    
- Les restrictions ont un impact sur l'utilisation de la mémoire d'une table. Un tableau fortement restreint avec un nombre important de lignes, telles qu'une table des matières, peut être susceptible de s'adapter à la mémoire pendant qu'une table de grande taille non restreinte ne l'est généralement pas. 
    
- Plusieurs des tables appartenant à MAPI, telles que l'État, le profil, le service de messagerie, le fournisseur et les tables de banque de messages, sont généralement contenues dans la mémoire. Il s'agit généralement de petites tables. Toutefois, il existe des exceptions. Par exemple, un fournisseur de profils serveur peut générer une table de profil plus grande qui ne pourra pas être ajustée.
    
Pour récupérer toutes les lignes d'une table qui tiendront dans la mémoire sans problème, appelez [HrQueryAllRows](hrqueryallrows.md), en définissant le nombre maximal de lignes sur zéro.
  
Pour récupérer toutes les lignes d'une table qui peuvent être dans la mémoire ou non, générant une erreur, appelez **HrQueryAllRows** en spécifiant un nombre maximal de lignes. Le nombre maximal de lignes doit être défini sur un nombre supérieur au nombre minimal de lignes nécessaires. Si un client doit accéder au moins à 50 lignes à partir d'une table de 300 lignes, le nombre maximal de lignes doit être défini sur au moins 51. 
  
Pour récupérer toutes les lignes d'une table qui ne sont pas censées tenir dans la mémoire, appelez la fonction [IMAPITable:: QueryRows](imapitable-queryrows.md) dans une boucle avec un nombre de lignes relativement faible, comme l'illustre l'exemple de code suivant: 
  
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

Lorsque cette boucle est terminée et que toutes les lignes de la table ont été traitées __ et que l'argument Crows a la valeur zéro, la position du curseur se trouve généralement en bas du tableau. 
  
## <a name="see-also"></a>Voir aussi

- [Tables MAPI](mapi-tables.md)

