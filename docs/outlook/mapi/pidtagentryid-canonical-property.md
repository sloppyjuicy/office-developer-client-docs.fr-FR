---
title: Propriété canonique PidTagEntryId
description: Décrit la propriété canonique PidTagEntryId, qui contient un identificateur d’entrée MAPI utilisé pour ouvrir et modifier les propriétés d’un objet MAPI particulier.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagEntryId
api_type:
- HeaderDef
ms.assetid: ca02e873-c2d2-4d58-8df8-c05fbcdc8fba
ms.openlocfilehash: 75caccf67b427d6fd12cd5c1ac0375efc8b41133
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770727"
---
# <a name="pidtagentryid-canonical-property"></a>Propriété canonique PidTagEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur d’entrée MAPI utilisé pour ouvrir et modifier les propriétés d’un objet MAPI particulier. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ENTRYID  <br/> |
|Identificateur :  <br/> |0x0FFF  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés d’ID  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété identifie un objet pour **qu’OpenEntry** instancie et donne accès à toutes ses propriétés via l’interface dérivée appropriée **d’IMAPIProp**. 
  
Cette propriété est l’une des propriétés d’adresse de base pour tous les utilisateurs de messagerie. 
  
Cette propriété peut contenir un identificateur à long terme ou à court terme. Les identificateurs à court terme sont plus faciles et plus rapides à construire, mais sont limités dans leur étendue et leur durée, généralement à la session et à la station de travail actuelles. Ils sont couramment utilisés pour les objets de nature temporaire, tels que les lignes de tableau ou les entrées de boîte de dialogue, puis abandonnés. Les identificateurs à long terme sont utilisés pour les objets de nature plus large et durable. 
  
Cette propriété est toujours disponible via la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) après le premier appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Certains fournisseurs de services peuvent le rendre disponible immédiatement après l’instanciation. Le fournisseur doit toujours retourner un identificateur d’entrée à long terme de **GetProps**. Par conséquent, pour convertir un identificateur à court terme en identificateur à long terme, ouvrez simplement l’objet et obtenez sa propriété via **GetProps**. 
  
Le tableau suivant résume les différences importantes entre cette propriété, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) et **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). 
  
|**Caractéristique**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Obligatoire sur les objets de pièce jointe  <br/> |Non  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire sur les objets de dossier  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire sur les objets du magasin de messages  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire sur les objets d’état  <br/> |Oui  <br/> |Non  <br/> |Non  <br/> |
|Créé par le client  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Disponible avant l’appel à **SaveChanges** <br/> |Dépend de l’implémentation du fournisseur  <br/> |Dépend de l’implémentation du fournisseur  <br/> |Pour les messages, Oui. Pour d’autres, dépend de l’implémentation du fournisseur. |
|Modification dans une opération de copie  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Modifiable par client après une copie  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Unique au sein de  <br/> |Monde entier  <br/> |Instance de fournisseur  <br/> |Monde entier  <br/> |
|Binaire comparable (comme avec memcmp)  <br/> |Aucune utilisation [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Oui  <br/> |Oui  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les listes d’utilisateurs, de contacts, de groupes et de ressources.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions e-mail standard Internet en objets de message.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère la commande et le flux des transferts de données entre un client et un serveur.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Gère la récupération des listes d’autorisations de dossiers stockées sur le serveur.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets de message et de calendrier lorsqu’elles agissent pour le compte d’un autre utilisateur.
    
[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)
  
> Spécifie le schéma et les méthodes utilisés pour demander des informations de disponibilité pour les utilisateurs et les ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

