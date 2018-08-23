---
title: Tables et utilisation de la mémoire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 383c03a00509447222204ab729c56f5eeac553df
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563015"
---
# <a name="tables-and-memory-usage"></a>Tables et utilisation de la mémoire

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Un aspect important connecté à extraire des données d’une table est de la mémoire. Manque de mémoire disponible peut entraîner [IMAPITable::QueryRows](imapitable-queryrows.md) et [HrQueryAllRows](hrqueryallrows.md) échec, retournez moins le nombre de lignes souhaité. Détermination de la méthode ou la fonction à utiliser pour récupérer des données de la table dépend de si la table peut être prévue pour tenir dans la mémoire et, si elle n’est pas le cas, si l’échec est acceptable. 
  
Car il n’est pas toujours facile à déterminer la quantité de données adapté en mémoire en même temps, MAPI fournit des instructions de base pour une application cliente ou le fournisseur de services à suivre. N’oubliez pas qu’il n’y a toujours exceptions, en fonction de l’implémentation de la table particulière et comment les données sous-jacentes sont stockées.
  
Les instructions suivantes peuvent servir à évaluer l’utilisation de la mémoire table :
  
- Les clients qui tolèrent occasionnellement travailler ensemble de la mémoire dans la plage mégaoctet et peuvent prendre qu’ils n’auront aucun problème de lecture d’un tableau entier en mémoire. 
    
- Restrictions ont une incidence sur l’utilisation d’une table de la mémoire. Un tableau avec un nombre important de lignes, par exemple une table des matières, strictement limité peut s’attendre à tenir dans la mémoire mais pas les généralement une table de grande taille illimitée. 
    
- Plusieurs tables appartenant à MAPI, tel que le statut, profils, service de message, fournisseur et tables de banque de messages, généralement contenir en mémoire. Il s’agit généralement de petites tables. Toutefois, il existe certaines exceptions. Par exemple, un fournisseur de profil sur le serveur peut générer une plus grande table profil qui ne sera pas en mesure d’adapter.
    
Pour récupérer toutes les lignes d’un tableau qui s’intègre à mémoire sans problème, appelez [HrQueryAllRows](hrqueryallrows.md), définissant le nombre maximal de lignes à zéro.
  
Pour récupérer toutes les lignes d’un tableau qui peut ou ne peut pas tenir dans la mémoire, génère une erreur, appelez **HrQueryAllRows** spécifiant un nombre maximal de lignes. Le nombre maximal de lignes doit être défini à un nombre supérieur au nombre minimal de lignes qui sont nécessaires. Si un client doit accéder au moins 50 lignes à partir d’une table de 300 lignes, le nombre maximal de lignes doit être défini au moins 51. 
  
Pour récupérer toutes les lignes d’un tableau qui n’est pas prévu pour tenir dans la mémoire, appelez [IMAPITable::QueryRows](imapitable-queryrows.md) dans une boucle avec un nombre de lignes relativement faible, comme l’illustre l’exemple de code suivant : 
  
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

Lorsque cette boucle se termine et toutes les lignes de la table ont été traitées et _cRows_ est égale à zéro, la position du curseur sera généralement en bas de la table. 
  
## <a name="see-also"></a>Voir aussi

- [Tables MAPI](mapi-tables.md)

