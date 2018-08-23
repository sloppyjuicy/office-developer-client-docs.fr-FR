---
title: Vue d'ensemble de la propriété MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e5b23f-1bdb-4fbf-a27d-e3301a359573
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 40a71592e658110dab81c9bcb4aec97f9930d014
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576476"
---
# <a name="mapi-property-overview"></a>Vue d'ensemble de la propriété MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une propriété est un attribut d’un objet MAPI. Propriétés décrivent un élément sur l’objet, telles que la ligne objet du message ou le type d’adresse d’un utilisateur de messagerie. MAPI définit de nombreuses propriétés, certaines pour décrire le nombre d’objets et certains qui conviennent uniquement pour un objet d’un type particulier. Clients et fournisseurs de services peuvent étendre ensemble de MAPI de propriétés prédéfinies en créant de nouvelles propriétés personnalisées. Les clients peuvent définir des propriétés décrivant les nouvelles classes de message et fournisseurs de services peuvent définir des propriétés pour exposer les fonctionnalités uniques de leur système de messagerie.
  
Propriétés peuvent être persistante ou temporaire. Propriétés qui sont conservées d’une session peuvent être stockées avec les données de leurs objets ou dans le profil. Propriétés temporaires existent uniquement pendant la durée de la session en cours. 
  
Clients et fournisseurs de services peuvent afficher les propriétés sur les utilisateurs disposant d’une table ou une feuille de propriétés. Tables fournissent aux utilisateurs un affichage en lecture seule de certaines des propriétés qui appartiennent à plusieurs objets. Les données sont affichées au format de ligne et de colonne, et chaque ligne représente un objet et une propriété de chaque colonne. Feuilles de propriétés sont des boîtes de dialogue à onglets affichent les propriétés associées pour un seul objet. Feuilles de propriétés peuvent fournir en lecture seule ou de lecture/écriture aux données. Si un utilisateur est autorisé à apporter des modifications dépend de l’implémentation de la feuille de propriétés.
  
L’interface [IMAPIProp](imapipropiunknown.md) est l’interface principale pour l’utilisation des propriétés. Tous les objets qui prennent en charge les propriétés implémenter **IMAPIProp**. **IMAPIProp** inclut des méthodes pour la récupération des valeurs de propriété, copie des propriétés, les modifications apportées et enregistrer ces changements, mappage entre les noms de propriétés et de leurs identificateurs et la récupération des informations sur une erreur précédente. 
  
Il existe plusieurs structures de données pour la description des propriétés et des informations sur les propriétés. Les structures plus couramment utilisés sont la structure [SPropValue](spropvalue.md) et la structure [SPropTagArray](sproptagarray.md) . La structure **SPropValue** contienne les trois éléments d’information qui décrivent une propriété : 
  
- Les données ou la valeur de la propriété.
    
- Type de données de la valeur de propriété, par exemple entier ou une valeur booléenne. 
    
- Valeur numérique dans une plage spécifique qui identifient les composants chargé de maintenance. Par exemple, il est une plage pour conserver le contenu définies par MAPI et une autre plage pour contenir les propriétés des messages de propriétés définies par un client pour une classe de message du message. 
    
Le type de propriété et l’identificateur sont combinées dans un seul composant appelé la balise de propriété. Balises de propriété sont des constantes qui peuvent être utilisés pour faire référence facilement à la propriété. Balises de propriété pour les propriétés définies par MAPI sont inclus dans le MAPITAGS. Fichier d’en-tête H et dans le membre **ulPropTag** d’une structure **SPropValue** . Clients et fournisseurs de services utilisent des balises de propriété pour identifier, récupérer et mettre à jour les propriétés correspondantes. 
  
La structure **SPropTagArray** est un tableau compté de balises de propriété. De nombreuses méthodes **IMAPIProp** et autres interfaces utilisent une structure **SPropTagArray** pour décrire les propriétés. 
  
## <a name="see-also"></a>Voir aussi



[Concepts MAPI](mapi-concepts.md)

