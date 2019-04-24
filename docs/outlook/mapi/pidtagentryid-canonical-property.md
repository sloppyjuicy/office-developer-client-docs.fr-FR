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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: feb34cdbf8ba917936c3272bcaaf6eff040ddc3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328587"
---
# <a name="pidtagentryid-canonical-property"></a>Propriété canonique PidTagEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur d'entrée MAPI utilisé pour ouvrir et modifier les propriétés d'un objet MAPI particulier. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ENTRYID  <br/> |
|Identificateur :  <br/> |0x0FFF  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés ID  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété identifie un objet pour **OpenEntry** à instancier et permet d'accéder à toutes ses propriétés via l'interface dérivée appropriée de **IMAPIProp**. 
  
Cette propriété est l'une des propriétés d'adresse de base pour tous les utilisateurs de messagerie. 
  
Cette propriété peut contenir un identificateur à long ou à court terme. Les identificateurs à court terme sont plus faciles et plus rapides à créer, mais sont limités en termes de portée et de durée, généralement à la session et à la station de travail en cours. Elles sont généralement utilisées pour les objets de nature temporaire, tels que les lignes de tableau ou les entrées de boîte de dialogue, puis abandonnées. Les identificateurs à long terme sont utilisés pour les objets d'un caractère plus large et durable. 
  
Cette propriété est toujours disponible par le biais de la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) qui suit le premier appel à la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Certains fournisseurs de services peuvent le mettre à disposition immédiatement après l'instanciation. Le fournisseur doit toujours renvoyer un identificateur d'entrée à long terme à partir de **GetProps**. Par conséquent, pour convertir un identificateur à court terme en un identificateur à long terme, il suffit d'ouvrir l'objet et d'obtenir sa propriété par le biais de **GetProps**. 
  
Le tableau suivant récapitule les différences importantes entre cette propriété, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) et **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). 
  
|**Caractéristique**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Obligatoire sur les objets Attachment  <br/> |Non  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire sur les objets Folder  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire sur les objets de banque de messages  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire sur les objets d'État  <br/> |Oui  <br/> |Non  <br/> |Non  <br/> |
|Créé par le client  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Disponible avant l'appel à **SaveChanges** <br/> |Dépend de l'implémentation du fournisseur  <br/> |Dépend de l'implémentation du fournisseur  <br/> |Pour les messages, oui. Pour d'autres, dépend de l'implémentation du fournisseur.  <br/> |
|Modifié dans une opération de copie  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Modifiable par le client après une copie  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Unique dans  <br/> |Tout le monde  <br/> |Instance de fournisseur  <br/> |Tout le monde  <br/> |
|Binaire comparable (comme avec memcmp)  <br/> |Ne pas utiliser [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Oui  <br/> |Oui  <br/> |
   
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les listes d'utilisateurs, de contacts, de groupes et de ressources.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> ConVertit des conventions de messagerie standard Internet en objets message.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l'ordre et le flux de transfert de données entre un client et un serveur.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Gère la récupération des listes d'autorisations de dossier stockées sur le serveur.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets message et Calendar lorsqu'ils agissent pour le compte d'un autre utilisateur.
    
[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)
  
> Spécifie le schéma et les méthodes qui sont utilisés pour demander des informations de disponibilité pour les utilisateurs et les ressources.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

