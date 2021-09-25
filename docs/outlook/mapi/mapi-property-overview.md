---
title: Vue d’ensemble de la propriété MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 02e5b23f-1bdb-4fbf-a27d-e3301a359573
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0f214cf8fab62850620b012b2cfd017b340dc013
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579515"
---
# <a name="mapi-property-overview"></a>Vue d’ensemble de la propriété MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une propriété est un attribut d’un objet MAPI. Les propriétés décrivent quelque chose sur l’objet, comme la ligne d’objet d’un message ou le type d’adresse d’un utilisateur de messagerie. MAPI définit de nombreuses propriétés, certaines pour décrire de nombreux objets et d’autres qui sont appropriées uniquement pour un objet d’un type particulier. Les clients et les fournisseurs de services peuvent étendre l’ensemble de propriétés prédéfinie mapi en créant des propriétés personnalisées. Les clients peuvent définir des propriétés pour décrire de nouvelles classes de messages, et les fournisseurs de services peuvent définir des propriétés pour exposer les fonctionnalités uniques de leur système de messagerie.
  
Les propriétés peuvent être persistantes ou temporaires. Les propriétés qui persistent d’une session à l’autre peuvent être stockées avec les données de leurs objets ou dans le profil. Les propriétés temporaires existent uniquement pour la durée de la session en cours. 
  
Les clients et les fournisseurs de services peuvent afficher les propriétés aux utilisateurs avec une table ou une feuille de propriétés. Les tableaux offrent aux utilisateurs une vue en lecture seule de certaines propriétés appartenant à plusieurs objets. Les données sont affichées au format de ligne et de colonne, chaque ligne représentant un objet et chaque colonne une propriété. Les feuilles de propriétés sont des boîtes de dialogue à onglets qui affichent les propriétés associées d’un seul objet. Les feuilles de propriétés peuvent fournir un accès en lecture seule ou en lecture/écriture aux données. L’implémenteur de la feuille des propriétés décide si un utilisateur est autorisé ou non à apporter des modifications.
  
[L’interface IMAPIProp](imapipropiunknown.md) est l’interface principale pour l’utilisation des propriétés. Tous les objets qui la prise en charge des propriétés **implémentent IMAPIProp**. **IMAPIProp** inclut des méthodes pour récupérer des valeurs de propriétés, copier des propriétés, apporter des modifications et enregistrer ces modifications, établir un mappage entre les noms de propriétés et leurs identificateurs et récupérer des informations sur une erreur précédente. 
  
Il existe plusieurs structures de données pour décrire les propriétés et les informations sur les propriétés. Les structures les plus couramment utilisées sont la structure [SPropValue](spropvalue.md) et la structure [SPropTagArray.](sproptagarray.md) La structure **SPropValue** contient les trois éléments d’informations qui décrivent une propriété : 
  
- Données, ou valeur, de la propriété.
    
- Type de données de la valeur de la propriété, par exemple, integer ou Boolean. 
    
- Valeur numérique dans une plage particulière qui identifie de manière unique la propriété et le composant responsables de sa maintenance. Par exemple, il existe une plage pour contenir les propriétés de contenu de message définies par MAPI et une autre plage pour contenir les propriétés de contenu de message définies par un client pour une classe de message personnalisée. 
    
Le type de propriété et l’identificateur sont combinés en un seul composant appelé balise de propriété. Les balises de propriété sont des constantes qui peuvent être utilisées pour faire facilement référence à la propriété. Les balises de propriété pour les propriétés définies par MAPI sont incluses dans MAPITAGS. Fichier d’en-tête H et dans le **membre ulPropTag** d’une structure **SPropValue.** Les clients et les fournisseurs de services utilisent des balises de propriété pour identifier, récupérer et mettre à jour les propriétés correspondantes. 
  
La structure **SPropTagArray est** un tableau compté de balises de propriété. De nombreuses méthodes dans **IMAPIProp** et d’autres interfaces utilisent une structure **SPropTagArray** pour décrire les propriétés. 
  
## <a name="see-also"></a>Voir aussi



[Concepts MAPI](mapi-concepts.md)

