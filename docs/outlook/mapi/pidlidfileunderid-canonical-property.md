---
title: Propriété canonique PidLidFileUnderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidFileUnderId
api_type:
- COM
ms.assetid: 917431a9-fd90-4b4d-b042-886e3dbf47c0
description: Indique comment générer et recompiler la valeur de la propriété dispidFileUnder lorsque d’autres propriétés de nom de contact changent.
ms.openlocfilehash: b28d1792ec9057bd7eb6c3ffbae825967ac9df00
ms.sourcegitcommit: 2d91bac3a93af3f1f73098f484000ba2a6377cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2022
ms.locfileid: "63558751"
---
# <a name="pidlidfileunderid-canonical-property"></a>Propriété canonique PidLidFileUnderId
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique comment générer et recompiler la valeur de la propriété **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) lorsque d’autres propriétés de nom de contact changent.
  
|**Propriété**|**Valeur**|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidFileUnderId  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID long (LID) :  <br/> |0x00008006  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété est manquante ou définie sur une valeur non détaillée dans le tableau [ci-dessous ou dans [MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), l’application peut choisir sa propre logique pour recompiler la valeur de **dispidFileUnder** à mesure que d’autres propriétés de nom de contact changent. 
  
Dans le tableau suivant, la notation \<PropertyName> est utilisée pour spécifier « la valeur de PropertyName ». Par exemple, si la valeur de la propriété **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) est « Smith » et que la valeur de la propriété **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) est « Ben », « »\<PidTagGivenName> \<PidTagSurname>spécifie la chaîne « Ben Smith ». Dans le tableau, « \r » spécifie un caractère de retour chariot, « \n » spécifie un caractère de retour de ligne et \<space> représente un espace.
  
|**Valeur de la **propriété dispidFileUnderId****|**Description de la **propriété dispidFileUnder****|
|:-----|:-----|
|0x00000000  <br/> |Vide PT_UNICODE. |
|0x00003001  <br/> |"\<PidTagDisplayName\>"  <br/> |
|0x00003A06  <br/> |"\<PidTagGivenName\>"  <br/> |
|0x00003A11  <br/> |"\<PidTagSurname\>"  <br/> |
|0x00003A16  <br/> |"\<PidTagCompanyName\>"  <br/> |
|0x00008017  <br/> |"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"  <br/> |
|0x00008018  <br/> |«\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<PidTagMiddleName\>\<space\>\<PidTagGivenName\>\<space\> »  <br/> |
|0x00008019  <br/> |« \<PidTagSurname\>,\<space\>\<PidTagMiddleName\>\<PidTagGivenName\>\<space\>\r\n»\<PidTagCompanyName\>  <br/> |
|0x00008030  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"  <br/> |
|0x00008031  <br/> |"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"  <br/> |
|0x00008032  <br/> |«\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<PidTagMiddleName\>»  <br/> |
|0x00008033  <br/> |«\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagMiddleName\>\<space\>\<PidTagGivenName\>\<space\>»  <br/> |
|0x00008034  <br/> |«\<PidTagSurname\>\<PidTagMiddleName\>\<PidTagGivenName\>\<space\>\r\n»\<PidTagCompanyName\>  <br/> |
|0x00008035  <br/> |«\<PidTagSurname\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGivenName\>\r\n»\<PidTagCompanyName\>  <br/> |
|0x00008036  <br/> |"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"  <br/> |
|0x00008037  <br/> |"\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagSurname\>\<space\>\<PidTagGeneration\>"  <br/> |
|0x00008038  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"  <br/> |
|0xfffffffd  <br/> |Spécifie que, lors de l’affichage du contact, l’application doit essayer d’utiliser la valeur actuelle de **dispidFileUnder** et d’autres propriétés de contact pour trouver une « meilleure correspondance » pour **dispidFileUnderId** avec l’une des valeurs précédentes de ce tableau. |
|0xfffffffe  <br/> |Spécifie que, lors de l’affichage du contact, l’application doit choisir les valeurs par défaut appropriées (en fonction des paramètres régionaux de langue) pour **dispidFileUnderId** et mettre à jour **dispidFileUnder** pour qu’elle corresponde au choix. |
|0xffffffff  <br/> |**dispidFileUnder** est une propriété fournie par l’PT_UNICODE et ne doit pas être modifiée lorsqu’une autre propriété de nom de contact change. |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)

> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
 
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)

> Spécifie les propriétés et opérations autorisées pour les contacts et les listes de distribution personnelles.

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h

> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi

[Propriétés MAPI](mapi-properties.md)  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)
