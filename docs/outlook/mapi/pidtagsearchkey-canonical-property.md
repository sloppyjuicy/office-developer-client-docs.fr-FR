---
title: Propriété canonique PidTagSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345464"
---
# <a name="pidtagsearchkey-canonical-property"></a>Propriété canonique PidTagSearchKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une clé comparable binaire qui identifie les objets corrélés pour une recherche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SEARCH_KEY  <br/> |
|Identificateur :  <br/> |0x300B  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Propriétés ID  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété fournit un suivi pour les objets associés, tels que les copies de messages, et facilite la recherche des occurrences indésirables, telles que des destinataires en double.
  
MAPI utilise des règles spécifiques pour la création de clés de recherche pour les destinataires des messages. La clé de recherche est formée en concaténant le type d'adresse (en majuscules), le signe deux-points «:», l'adresse de messagerie au format canonique et le caractère null de fin. Formulaire canonique cela signifie que les adresses respectant la casse apparaissent dans la casse correcte et que les adresses qui ne respectent pas la casse sont converties en majuscules. Ceci est important en matière de conservation des corrélations entre les messages.
  
Pour les objets message, cette propriété est disponible par le biais de la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) immédiatement après la création de messages. Pour les autres objets, elle est disponible après le premier appel à la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Étant donné que cette propriété est modifiable, il est peu fiable de l'obtenir via **GetProps** jusqu'à ce qu'un appel de **SaveChanges** ait validé des valeurs définies ou modifiées par la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) . 
  
Pour les profils, MAPI fournit également une section de profil codé en dur nommée **MUID_PROFILE_INSTANCE**, avec cette propriété comme propriété unique. Cette clé est unique dans tous les profils créés, et peut être plus fiable que la propriété **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)), qui peut être, par exemple, supprimée et recréée avec le même nom.
  
Le tableau suivant récapitule les différences importantes entre le **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) et cette propriété.
  
|**Caractéristique**|PR_ENTRYID * * * *|PR_RECORD_KEY * * * *|PR_SEARCH_KEY * * * *|
|:-----|:-----|:-----|:-----|
|Obligatoire sur les objets Attachment  <br/> |Non  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire sur les objets Folder  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire sur les objets de banque de messages  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Obligatoire sur les objets d'État  <br/> |Oui  <br/> |Non  <br/> |Non  <br/> |
|Pouvant être créé par le client  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Disponible avant **SaveChanges** <br/> |Dépend de l'implémentation du fournisseur  <br/> |Dépend de l'implémentation du fournisseur  <br/> |Pour les messages, oui. Pour d'autres, cela dépend de l'implémentation du fournisseur.  <br/> |
|Modifié dans une opération de copie  <br/> |Oui  <br/> |Oui  <br/> |Non  <br/> |
|Modifiable par le client après une copie  <br/> |Non  <br/> |Non  <br/> |Oui  <br/> |
|Unique au sein de...  <br/> |Tout le monde  <br/> |Instance de fournisseur  <br/> |Tout le monde  <br/> |
|Binaire comparable (comme avec memcmp)  <br/> |Non--utiliser [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Oui  <br/> |Oui  <br/> |
   
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



[Propriété canonique PidTagResponsibility](pidtagresponsibility-canonical-property.md)
  
[Propriété canonique PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

