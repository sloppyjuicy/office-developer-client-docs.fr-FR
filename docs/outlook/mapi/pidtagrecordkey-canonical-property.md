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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7a3ae7db1fb97e97f7d0939b67f139af62477bf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355264"
---
# <a name="pidtagrecordkey-canonical-property"></a>Propriété canonique PidTagRecordKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur unique et comparable pour un objet spécifique.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RECORD_KEY  <br/> |
|Identificateur :  <br/> |0x0FF9  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés ID  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété facilite la recherche des références à un objet, telles que la recherche de sa ligne dans une table des matières. Cette propriété ne peut pas être utilisée pour ouvrir un objet; Utilisez l'identificateur d'entrée à cet effet.
  
Un sous-objet de pièce jointe doit être identifié de manière unique dans un message par cette propriété. Cet identificateur est la seule caractéristique de pièce jointe garantie de rester identique une fois que le message a été fermé et rouvert. Le fournisseur de banque doit conserver cette propriété entre les sessions pour garantir cette garantie.
  
Pour les dossiers, cette propriété contient une clé utilisée dans la table de hiérarchie des dossiers. En règle générale, il s'agit de la même valeur que celle fournie par la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
Pour les banques de messages, cette propriété est identique à la propriété **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)).
  
Dans un objet de banque de messages, cette propriété doit être unique dans tous les fournisseurs de magasins. Pour ce faire, vous pouvez combiner la valeur de la propriété **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) pour le magasin (unique à ce type de fournisseur) avec une structure [GUID](guid.md) ou une autre valeur propre à la Banque de messages spécifique. 
  
Cette propriété est toujours disponible par le biais de la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) qui suit le premier appel à la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Certains fournisseurs peuvent le mettre à disposition immédiatement après l'instanciation. 
  
Un client ou un fournisseur de services peut comparer les valeurs de cette propriété à l'aide de memcmp. Cela n'est pas possible pour les valeurs d'identificateur d'entrée. Toutefois, cette propriété est garantie unique dans le même conteneur de banque de messages ou de carnet d'adresses; deux objets de différents conteneurs peuvent avoir la même valeur de cette propriété.
  
La seule différence entre les clés record et Search est que la clé d'enregistrement est propre à l'objet, tandis que la clé de recherche peut être copiée vers d'autres objets. Par exemple, deux copies de l'objet peuvent avoir la même valeur **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), mais elles doivent avoir des valeurs différentes pour cette propriété.
  
Le tableau suivant récapitule les différences importantes entre les propriétés **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) et cette propriété. 
  
|**Caractéristique**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Obligatoire sur les objets Attachment  <br/> |Non  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire sur les objets Folder  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire sur les objets de banque de messages  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire sur les objets d'État  <br/> |Oui  <br/> |Non  <br/> |Non  <br/> |
|Pouvant être créé par le client  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Disponible avant un appel à **SaveChanges** <br/> |Zipper  <br/> |Zipper  <br/> |Messages Oui d'autres personnes  <br/> |
|Modifié dans une opération de copie  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Modifiable par un client après une copie  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Unique au sein de...  <br/> |Tout le monde  <br/> |Instance de fournisseur  <br/> |Tout le monde  <br/> |
|Binaire comparable (comme avec memcmp)  <br/> |Non--utiliser **IMAPISupport:: CompareEntryIDs** <br/> |Oui  <br/> |Oui  <br/> |
   
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les listes d'utilisateurs, de contacts, de groupes et de ressources.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

