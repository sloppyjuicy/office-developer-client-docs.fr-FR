---
title: Propriété canonique PidLidFileUnderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnderId
api_type:
- COM
ms.assetid: 917431a9-fd90-4b4d-b042-886e3dbf47c0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7af30866a5fd2846327223b7a58c6de91f5fef7a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397190"
---
# <a name="pidlidfileunderid-canonical-property"></a>Propriété canonique PidLidFileUnderId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie comment générer et recalculer la valeur de la propriété **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) lorsque propriétés modifier le nom de contact.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidFileUnderId  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID de type long (capot) :  <br/> |0x00008006  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété est manquant ou une valeur non détaillés dans le tableau ci-dessous ou dans [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), l’application peut choisir sa propre logique de recalculer la valeur de la **dispidFileUnder** d' autres propriétés comme nom du contact. 
  
Dans le tableau suivant, la notation <PropertyName> est utilisé pour spécifier « la valeur de PropertyName ». Par exemple, si la valeur de la propriété **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) est « Smith », et la valeur de la propriété **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) est « Ben », puis «<PidTagGivenName> <PidTagSurname>» spécifie la chaîne « Ben Smith ». Dans le tableau, « \r » spécifie un caractère de retour chariot, « \n » spécifie un caractère de saut de ligne, et <space> représente un espace.
  
|**Valeur de la propriété **dispidFileUnderId****|**Description de la propriété **dispidFileUnder****|
|:-----|:-----|
|0x00000000  <br/> |PT_UNICODE vide.  <br/> |
|0x00003001  <br/> |«\<PidTagDisplayName\>»  <br/> |
|0x00003A06  <br/> |«\<PidTagGivenName\>»  <br/> |
|0x00003A11  <br/> |«\<PidTagSurname\>»  <br/> |
|0x00003A16  <br/> |«\<PidTagCompanyName\>»  <br/> |
|0x00008017  <br/> |«\<PidTagSurname\>,\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»  <br/> |
|0x00008018  <br/> |«\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»  <br/> |
|0x00008019  <br/> |«\<PidTagSurname\>,\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>»  <br/> |
|0x00008030  <br/> |«\<PidTagSurname\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»  <br/> |
|0x00008031  <br/> |«\<PidTagSurname\>\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»  <br/> |
|0x00008032  <br/> |«\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»  <br/> |
|0x00008033  <br/> |«\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>»  <br/> |
|0x00008034  <br/> |«\<PidTagSurname\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>»  <br/> |
|0x00008035  <br/> |«\<PidTagSurname\>\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>»  <br/> |
|0x00008036  <br/> |«\<PidTagSurname\>\<espace\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\<espace\>\<PidTagGeneration\>»  <br/> |
|0x00008037  <br/> |«\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\<espace\>\<PidTagSurname\>\<espace\>\<PidTagGeneration\>»  <br/> |
|0x00008038  <br/> |«\<PidTagSurname\>\<PidTagGivenName\>\<espace\>\<PidTagMiddleName\>\<espace\>\<PidTagGeneration\>»  <br/> |
|0xfffffffd  <br/> |Spécifie que, lorsque vous affichez le contact, l’application doit essayer d’utiliser la valeur actuelle de **dispidFileUnder** et d’autres propriétés de contact pour rechercher « au mieux » **dispidFileUnderId** à une des valeurs dans le tableau précédents.  <br/> |
|0xFFFFFFFE  <br/> |Spécifie que, lorsque vous affichez le contact, l’application doit choisir les valeurs par défaut approprié (en fonction des paramètres régionaux de langue) pour **dispidFileUnderId** et **dispidFileUnder** pour faire correspondre le choix de mettre à jour.  <br/> |
|0xFFFFFFFF  <br/> |**dispidFileUnder** est une PT_UNICODE fourni par l’utilisateur et ne doit pas être modifiée lors de la modification d’une autre propriété nom du contact.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

