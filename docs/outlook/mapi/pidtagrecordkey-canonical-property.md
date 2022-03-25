---
title: Propriété canonique PidTagRecordKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRecordKey
api_type:
- COM
ms.assetid: a12fb9a2-799d-4112-b26c-4b2854c47cc2
description: Contient un identificateur unique comparable au binaire pour un objet spécifique. Cette propriété ne peut pas être utilisée pour ouvrir un objet.
ms.openlocfilehash: 4dfc11a74f0dce6e5f444209c3a6dffee24dd31f
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63780927"
---
# <a name="pidtagrecordkey-canonical-property"></a>Propriété canonique PidTagRecordKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur unique comparable au binaire pour un objet spécifique.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECORD_KEY  <br/> |
|Identificateur :  <br/> |0x0FF9  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés de l’ID  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété facilite la recherche de références à un objet, telles que la recherche de sa ligne dans une table des matières. Cette propriété ne peut pas être utilisée pour ouvrir un objet ; utilisez l’identificateur d’entrée à cet effet.
  
Un sous-objet de pièce jointe doit être identifié de manière unique dans un message par cette propriété. Cet identificateur est la seule caractéristique de pièce jointe qui reste identique une fois le message fermé et rouvert. Le fournisseur de magasin doit conserver cette propriété entre les sessions pour garantir cette garantie.
  
Pour les dossiers, cette propriété contient une clé utilisée dans la table de hiérarchie de dossiers. En règle générale, il s’agit de la même valeur que celle fournie par la **propriété PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
Pour les magasins de messages, cette propriété est identique à la **propriété PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)).
  
Dans un objet de magasin de messages, cette propriété doit être unique dans tous les fournisseurs de magasins. Pour ce faire, vous pouvez combiner la valeur de la propriété **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) de la boutique (propre à ce type de fournisseur) avec une structure [GUID](guid.md) ou une autre valeur propre à la magasin de messages spécifique. 
  
Cette propriété est toujours disponible via la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) après le premier appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Certains fournisseurs peuvent le rendre disponible immédiatement après l’ins instantiation. 
  
Un client ou un fournisseur de services peut comparer les valeurs de cette propriété à l’aide de memcmp. Cela n’est pas possible pour les valeurs d’identificateur d’entrée. Toutefois, il est garanti que cette propriété soit unique dans le même conteneur de carnet d’adresses ou de magasin de messages . deux objets provenant de conteneurs différents peuvent avoir la même valeur de cette propriété.
  
L’une des différences entre les clés d’enregistrement et de recherche est que la clé d’enregistrement est spécifique à l’objet, alors que la clé de recherche peut être copiée dans d’autres objets. Par exemple, deux copies de l’objet peuvent avoir la même valeur **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), mais doivent avoir des valeurs différentes pour cette propriété.
  
Le tableau suivant récapitule les différences importantes entre **PR_ENTRYID,** **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) et cette propriété. 
  
|**Caractéristique**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Obligatoire pour les objets pièce jointe  <br/> |Non  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire pour les objets de dossier  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire sur les objets de la boutique de messages  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire sur les objets d’état  <br/> |Oui  <br/> |Non  <br/> |Non  <br/> |
|Créatable par client  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Disponible avant un appel **à SaveChanges** <br/> |Peut-être  <br/> |Peut-être  <br/> |Messages Oui, d’autres, peut-être  <br/> |
|Modifié dans une opération de copie  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Modification possible par un client après une copie  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Unique dans ... |Monde entier  <br/> |Instance de fournisseur  <br/> |Monde entier  <br/> |
|Binary comparable (comme avec memcmp)  <br/> |No -- use **IMAPISupport:: CompareEntryIDs** <br/> |Oui  <br/> |Oui  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

