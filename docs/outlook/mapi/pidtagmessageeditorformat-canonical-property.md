---
title: Propriété canonique PidTagMessageEditorFormat
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageEditorFormat
api_type:
- HeaderDef
ms.assetid: 197b21ed-9f2f-425f-a6ed-cae1208fa2ca
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 029df4397f4d24c7c111d2017d34e6403df367d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325633"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a>Propriété canonique PidTagMessageEditorFormat

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie le format qu'un éditeur doit utiliser pour afficher un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MSG_EDITOR_FORMAT  <br/> |
|Identificateur :  <br/> |0x5909  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs possibles pour **PR_MSG_EDITOR_FORMAT** peuvent être l'une des valeurs suivantes: 
  
|**Value**|**Description**|
|:-----|:-----|
|**EDITOR_FORMAT_DONTKNOW** <br/> |Le format de l'éditeur à utiliser est inconnu.  <br/> |
|**EDITOR_FORMAT_PLAINTEXT** <br/> |L'éditeur doit afficher le message au format texte brut.  <br/> |
|**EDITOR_FORMAT_HTML** <br/> |L'éditeur doit afficher le message au format HTML.  <br/> |
|**EDITOR_FORMAT_RTF** <br/> |L'éditeur doit afficher le message au format RTF.  <br/> |
   
Par défaut, les messages électroniques (avec la classe de message **IPM. Note** ou avec une classe de message personnalisée dérivée de **IPM. Remarque**) envoyé à partir d'un compte de messagerie POP3/SMTP sont envoyés au format TNEF (Transport Neutral encapsulAtion format). La propriété **PR_MSG_EDITOR_FORMAT** peut être utilisée pour appliquer uniquement du texte brut, et non au format TNEF, lors de l'envoi d'un message. Si **PR_MSG_EDITOR_FORMAT** est défini sur **EDITOR_FORMAT_PLAINTEXT**, le message est envoyé en tant que texte brut sans TNEF. Si **PR_MSG_EDITOR_FORMAT** est défini sur **EDITOR_FORMAT_RTF**, le codage TNEF est implicitement activé et le message est envoyé à l'aide du format Internet par défaut spécifié dans le client Outlook.
  
Il existe deux autres façons d'appliquer le format TNEF lors de l'envoi d'un message.
  
- La définition de la propriété nommée **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) sur true sur un message indique que le format TNEF doit être inclus lors de la conversion du message MAPI en MIME/SMTP. Notez que **dispidUseTNEF** s'applique uniquement lorsque le message est envoyé à partir d'un compte de messagerie POP3/SMTP, et ne s'applique pas lorsque le message est envoyé par d'autres fournisseurs, tels que Microsoft Exchange Server. **dispidUseTNEF** remplace le paramètre dans **PR_MSG_EDITOR_FORMAT**.
    
- L'utilisation de l'indicateur **CCSF_USE_TNEF** lors de l'appel de [IConverterSession:: MAPItoMIMEStm](iconvertersession-mapitomimestm.md) pour convertir un message MAPI sortant en flux MIME peut également appliquer le format TNEF. Cela s'applique même si **dispidUseTNEF** n'est pas défini. 
    
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Définit les structures de données de base qui sont utilisées dans les opérations distantes.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.
    
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

