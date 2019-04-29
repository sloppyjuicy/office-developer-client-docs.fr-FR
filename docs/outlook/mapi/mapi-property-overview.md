---
title: Vue d’ensemble de la propriété MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e5b23f-1bdb-4fbf-a27d-e3301a359573
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 99887bab2b576e6e6c05414ee9daf1bd6e8d0463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408326"
---
# <a name="mapi-property-overview"></a>Vue d’ensemble de la propriété MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une propriété est un attribut d'un objet MAPI. Les propriétés décrivent un aspect de l'objet, comme la ligne d'objet d'un message ou le type d'adresse d'un utilisateur de messagerie. MAPI définit un grand nombre de propriétés, certaines pour décrire de nombreux objets et certains d'entre eux sont appropriés uniquement pour un objet d'un type particulier. Les clients et les fournisseurs de services peuvent étendre l'ensemble de propriétés prédéfinies MAPI en créant de nouvelles propriétés personnalisées. Les clients peuvent définir des propriétés pour décrire de nouvelles classes de messages, et les fournisseurs de services peuvent définir des propriétés pour exposer les fonctionnalités uniques de leur système de messagerie.
  
Les propriétés peuvent être permanentes ou temporaires. Les propriétés qui persistent d'une session à l'autres peuvent être stockées avec les données de leurs objets ou dans le profil. Les propriétés temporaires existent uniquement pendant la durée de la session en cours. 
  
Les clients et les fournisseurs de services peuvent afficher les propriétés aux utilisateurs à l'aide d'une table ou d'une feuille de propriétés. Les tableaux fournissent aux utilisateurs une vue en lecture seule de certaines propriétés appartenant à plusieurs objets. Les données sont affichées dans le format de ligne et de colonne, chaque ligne représentant un objet et chaque colonne une propriété. Les feuilles de propriétés sont des boîtes de dialogue à onglets qui affichent les propriétés connexes d'un objet unique. Les feuilles de propriétés peuvent fournir un accès en lecture seule ou en lecture/écriture aux données. Le fait que l'utilisateur soit ou non autorisé à effectuer des modifications dépend de l'implémenteur de la feuille de propriétés.
  
L'interface [IMAPIProp](imapipropiunknown.md) est l'interface principale permettant d'utiliser les propriétés. Tous les objets qui prennent en charge les propriétés implémentent **IMAPIProp**. **IMAPIProp** inclut des méthodes pour extraire des valeurs de propriétés, copier des propriétés, apporter des modifications et enregistrer ces modifications, mapper entre les noms de propriétés et leurs identificateurs, et extraire des informations sur une erreur précédente. 
  
Il existe plusieurs structures de données pour décrire des propriétés et des informations sur les propriétés. Les structures les plus couramment utilisées sont la structure [SPropValue](spropvalue.md) et la structure [SPropTagArray](sproptagarray.md) . La structure **SPropValue** contient les trois informations qui décrivent une propriété: 
  
- Données, ou valeur, de la propriété.
    
- Type de données de la valeur de la propriété, comme Integer ou Boolean. 
    
- Valeur numérique dans une plage particulière qui identifie de manière unique la propriété et le composant chargé de la maintenance. Par exemple, il existe une plage pour contenir les propriétés de contenu de message définies par MAPI, ainsi qu'une autre plage pour contenir les propriétés de contenu de message définies par un client pour une classe de message personnalisée. 
    
Le type de propriété et l'identificateur sont combinés en un seul composant appelé la balise de propriété. Les balises de propriété sont des constantes qui peuvent être utilisées pour faire référence facilement à la propriété. Les balises de propriété pour les propriétés définies par MAPI sont incluses dans le MAPITAGS. H et dans le membre **ulPropTag** d'une structure **SPropValue** . Les clients et les fournisseurs de services utilisent des balises de propriété pour identifier, récupérer et mettre à jour les propriétés correspondantes. 
  
La structure **SPropTagArray** est un tableau compté de balises de propriété. De nombreuses méthodes dans **IMAPIProp** et d'autres interfaces utilisent une structure **SPropTagArray** pour décrire les propriétés. 
  
## <a name="see-also"></a>Voir aussi



[Concepts MAPI](mapi-concepts.md)

