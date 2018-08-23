---
title: Propriété canonique PidTagRecordKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecordKey
api_type:
- COM
ms.assetid: a12fb9a2-799d-4112-b26c-4b2854c47cc2
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 9add9246cdfb22f7c5ad579f425932f49d4a9ecd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581243"
---
# <a name="pidtagrecordkey-canonical-property"></a>Propriété canonique PidTagRecordKey

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un identificateur unique comparable binaire pour un objet spécifique.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECORD_KEY  <br/> |
|Identificateur :  <br/> |0x0FF9  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés ID  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété facilite la localisation des références à un objet, telles que la recherche de sa ligne dans une table des matières. Cette propriété ne peut pas être utilisée pour ouvrir un objet ; Utilisez l’identificateur d’entrée à cet effet.
  
Un sous-objet de pièce jointe doit être identifiée dans un message par cette propriété. Cet identificateur est la seule caractéristique de pièce jointe garantie reste le même une fois que le message est fermé et rouverte. Le fournisseur de banque doit conserver cette propriété entre les sessions pour s’assurer de cette garantie.
  
Pour les dossiers, cette propriété contient une clé utilisée dans la table de hiérarchie de dossier. Il s’agit généralement de la même valeur que celles fournies par la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
Pour les banques de messages, cette propriété est identique à la propriété **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)).
  
Dans un objet de banque de messages, cette propriété doit être unique parmi tous les fournisseurs de magasins. Pour ce faire consiste à combiner la valeur de la propriété **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) pour le magasin (unique pour ce type de fournisseur) avec une structure [GUID](guid.md) ou une autre valeur unique dans le magasin de message spécifique. 
  
Cette propriété est toujours disponible par le biais de la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du premier appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) qui suit. Certains fournisseurs peuvent rendre disponibles immédiatement après l’instanciation. 
  
Un client ou fournisseur de services comparer les valeurs de cette propriété à l’aide de memcmp. Il n’est pas possible, pour les valeurs d’identificateur d’entrée. Toutefois, cette propriété est garantie être uniques au sein de la banque de messages même ou ; conteneur de carnets d’adresses deux objets provenant de différents conteneurs peuvent avoir la même valeur de cette propriété.
  
Une distinction entre les clés de recherche et d’enregistrement est la clé d’enregistrement spécifique à l’objet, tandis que la clé de recherche peut être copiée à d’autres objets. Par exemple, deux copies de l’objet peuvent avoir la même valeur de **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), mais doivent avoir des valeurs différentes pour cette propriété.
  
Le tableau suivant récapitule les différences importantes entre **PR_ENTRYID**, **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) et cette propriété. 
  
|**Caractéristique**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Requis sur les objets attachment  <br/> |Non  <br/> |Oui  <br/> |Non  <br/> |
|Requis sur les objets de dossier  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Requis sur les objets de banque de messages  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Requis sur les objets d’état  <br/> |Oui  <br/> |Non  <br/> |Non  <br/> |
|Qui peut être créé par client  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Disponibles avant un appel à **SaveChanges** <br/> |Peut-être  <br/> |Peut-être  <br/> |Messages d’autres personnes Oui peut-être  <br/> |
|Modification dans une opération de copie  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Modifiable par un client après une copie  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Unique au sein de...  <br/> |Monde entier  <br/> |Instance de fournisseur  <br/> |Monde entier  <br/> |
|Binaire comparable (comme avec memcmp)  <br/> |No : utilisez **IMAPISupport :: CompareEntryIDs** <br/> |Oui  <br/> |Oui  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

