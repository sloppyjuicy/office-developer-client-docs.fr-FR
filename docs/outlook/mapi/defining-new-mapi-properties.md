---
title: Définition des nouvelles propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a2325ea-ddfa-480f-b65f-f5b20471fb40
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f922ee95cda84311d840aa9de339883c57efba56
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590322"
---
# <a name="defining-new-mapi-properties"></a>Définition des nouvelles propriétés MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
En dépit de nombreuses propriétés fournis par MAPI pour une utilisation par les clients et les fournisseurs de services, MAPI permet de nouvelles propriétés à créer si nécessaire. Certains scénarios valides pour la définition des nouvelles propriétés publiques incluent un client de création de propriétés pour prendre en charge une nouvelle classe de message et un fournisseur de services créer de nouvelles propriétés pour exposer les fonctionnalités de système de messagerie unique.
  
En règle générale, il n’est pas valide pour un fournisseur de service à définir de nouvelles propriétés pour une classe d’objet ou de message MAPI existante. Un des principaux avantages de l’utilisation de MAPI est que des identificateurs standards et mises en forme d’un grand nombre de système de messagerie éléments sont-ils, permettant aux utilisateurs de façon transparente combiner des fournisseurs de services. Fournisseurs de services qui utilisent les propriétés non standard ne fonctionnent pas aussi avec les autres fournisseurs de services. 
  
Les clients peuvent créer des propriétés de contenu pour les nouvelles classes de message par :
  
- À l’aide des identificateurs de propriété au sein d’une plage déterminée pour les propriétés contenu spécifique à la classe de message.
    
    - Ou -
    
- À l’aide des propriétés nommées. 
    
La première option est préférable car tous les fournisseurs de service prennent en charge les propriétés nommées. MAPI définit deux plages distinctes pour les clients à utiliser pour les nouvelles propriétés de contenu spécifique à la classe de message :
  
- 0x6800 0x7BFF pour les propriétés transmissible
    
- 0x7C00 0x7FFF des propriétés nontransmittable
    
Identificateurs de propriété doivent se situer dans des plages prédéfinies pour éviter les conflits entre les propriétés définies par différents fournisseurs ou des utilisateurs. Toutefois, les utilisateurs des propriétés de ces plages ne peut pas faire des suppositions quant le comportement des propriétés. Chaque client qui crée une nouvelle classe de message dispose d’un accès à ces plages ; une propriété avec l' identificateur _xxxx_ peut entraîner le comportement d’une classe de message et un autre comportement pour une autre classe de message. 
  
Propriétés nommées sont utilisées pour garantir qu'une propriété spécifique est unique à une classe de message. Identificateurs de propriété nommée Démarrer dans la plage 0 x 8000. Les clients définissent un ou plusieurs noms et puis appelez la méthode de [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) de la banque de messages pour associer un identificateur de chaque nom. Propriétés nommées utilisable par les clients ou fournisseurs de services pour définir de nouvelles propriétés pour tout objet que si le propriétaire de l’objet prend en charge les propriétés nommées. Les utilisateurs de ces propriétés appeler **GetIDsFromNames** et une méthode **IMAPIProp** connexe, [GetNamesFromIDs](imapiprop-getnamesfromids.md), une correspondance entre un nom et son identificateur.
  
Toutes les propriétés, nouvelle ou existantes, doivent utiliser l’ensemble des types de propriété prédéfinie. Nouveaux types de propriété ne peut pas être ajoutés et les types existants ne peuvent pas être modifiés ou supprimés. Propriétés simples, petites, telles que les propriétés d’entier seul caractère ou 16 bits, peuvent être stockées dans un type approprié. Par exemple, des entiers peuvent être stockés comme **ULONG** et les chaînes peuvent être stockées en tant que **PT_STRING8**. 
  
Utiliser le type **PT_BINARY** pour indiquer un tableau d’octets comptés. Ce type de propriété est utile pour étendre les types de données pouvant être stockés dans un objet. Octets sont transmis dans l’ordre et sans les hypothèses sur la signification des données. Lorsqu’une application cliente lit les données à partir de ce type de propriété, les données sont identiques par rapport à la façon dont elle a été stockée. Le client doit effectuer n’importe quel octet nécessaire échange lors du déplacement des données entre les processeurs. 
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

