---
title: Propriété canonique PidTagEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEntryId
api_type:
- HeaderDef
ms.assetid: ca02e873-c2d2-4d58-8df8-c05fbcdc8fba
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f3d49faba9d1e9cc8609ee55f7fb3c329e9ae947
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593038"
---
# <a name="pidtagentryid-canonical-property"></a>Propriété canonique PidTagEntryId

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un identificateur d’entrée MAPI utilisé pour ouvrir et modifier les propriétés d’un objet MAPI particulier. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ENTRYID  <br/> |
|Identificateur :  <br/> |0x0FFF  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés ID  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété identifie un objet pour **OpenEntry** instancier et donne accès à toutes ses propriétés via l’interface dérivée appropriée de **IMAPIProp**. 
  
Cette propriété est une des propriétés d’adresse de base pour tous les utilisateurs de messagerie. 
  
Cette propriété peut contenir une à long terme ou un identificateur à court terme. Identificateurs à court terme sont plus facile et plus rapide de construction, mais sont limités dans leur étendue et la durée, généralement pour la session en cours et la station de travail. Ils sont couramment utilisés pour les objets de nature temporaire, telles que les lignes ou les entrées de boîte de dialogue et puis abandonnés. Identificateurs à long terme sont utilisés pour les objets de nature plus vaste et durables. 
  
Cette propriété est toujours disponible par le biais de la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du premier appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) qui suit. Certains fournisseurs de services peuvent rendre disponibles immédiatement après l’instanciation. Le fournisseur doit toujours retourner un identificateur d’entrée à long terme de **GetProps**. Par conséquent, pour convertir un identificateur à court terme à long terme, simplement ouvrir l’objet et ses cette propriété via **GetProps**. 
  
Le tableau suivant récapitule les différences importantes entre cette propriété, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) et **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). 
  
|**Caractéristique**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Requis sur les objets attachment  <br/> |Non  <br/> |Oui  <br/> |Non  <br/> |
|Requis sur les objets de dossier  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Requis sur les objets de banque de messages  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Requis sur les objets d’état  <br/> |Oui  <br/> |Non  <br/> |Non  <br/> |
|Créé par client  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Avant l’appel à **SaveChanges** <br/> |Dépend de l’implémentation du fournisseur  <br/> |Dépend de l’implémentation du fournisseur  <br/> |Pour les messages, Oui. Pour d’autres personnes, dépend de l’implémentation du fournisseur.  <br/> |
|Modification dans une opération de copie  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Modifiable par client après une copie  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Unique dans  <br/> |Monde entier  <br/> |Instance de fournisseur  <br/> |Monde entier  <br/> |
|Binaire comparable (comme avec memcmp)  <br/> |Aucune utilisation [IMAPISupport :: CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Oui  <br/> |Oui  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet aux objets de message.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.
    
[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Gère la récupération des listes d’autorisations de dossier sont stockés sur le serveur.
    
[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.
    
[[MS-OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)
  
> Spécifie le schéma et les méthodes qui sont utilisées pour demander les informations de disponibilité des utilisateurs et des ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

