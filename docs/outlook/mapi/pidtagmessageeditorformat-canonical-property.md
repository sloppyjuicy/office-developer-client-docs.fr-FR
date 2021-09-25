---
title: Propriété canonique PidTagMessageEditorFormat
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageEditorFormat
api_type:
- HeaderDef
ms.assetid: 197b21ed-9f2f-425f-a6ed-cae1208fa2ca
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dd107de00ebc7ab55b6d255c4bc993d9c3210086
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560885"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a>Propriété canonique PidTagMessageEditorFormat

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie le format d’un éditeur à utiliser pour afficher un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MSG_EDITOR_FORMAT  <br/> |
|Identificateur :  <br/> |0x5909  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs possibles **pour PR_MSG_EDITOR_FORMAT** peuvent être l’une des suivantes : 
  
|**Valeur**|**Description**|
|:-----|:-----|
|**EDITOR_FORMAT_DONTKNOW** <br/> |Le format de l’éditeur à utiliser est inconnu.  <br/> |
|**EDITOR_FORMAT_PLAINTEXT** <br/> |L’éditeur doit afficher le message au format texte simple.  <br/> |
|**EDITOR_FORMAT_HTML** <br/> |L’éditeur doit afficher le message au format HTML.  <br/> |
|**EDITOR_FORMAT_RTF** <br/> |L’éditeur doit afficher le message au format Texte enrichi.  <br/> |
   
Par défaut, les messages électroniques (avec la classe de message **IPM. Remarque** ou avec une classe de message personnalisée dérivée **d’IPM. Remarque**) les messages envoyés à partir d’un compte de messagerie POP3/SMTP sont envoyés au format TNEF (Transport Neutral Encapsulation Format). La **PR_MSG_EDITOR_FORMAT** peut être utilisée pour appliquer uniquement le texte simple, et non le TNEF, lors de l’envoi d’un message. Si **PR_MSG_EDITOR_FORMAT** est définie sur **EDITOR_FORMAT_PLAINTEXT,** le message est envoyé en texte simple sans TNEF. Si **PR_MSG_EDITOR_FORMAT** est définie sur **EDITOR_FORMAT_RTF**, le codage TNEF est implicitement activé et le message est envoyé à l’aide du format Internet par défaut spécifié dans le client Outlook.
  
Il existe deux autres façons d’appliquer l’utilisation du TNEF lors de l’envoi d’un message.
  
- La définition de la propriété nommée **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) sur True dans un message indique que le TNEF doit être inclus lors de la conversion du message de MAPI en MIME/SMTP. Notez que **dispidUseTNEF** s’applique uniquement lorsque le message est envoyé à partir d’un compte de messagerie POP3/SMTP et ne s’applique pas lorsque le message est envoyé par d’autres fournisseurs, tels que Microsoft Exchange Server. **dispidUseTNEF** remplace le paramètre dans **PR_MSG_EDITOR_FORMAT**.
    
- L’utilisation de l’indicateur **CCSF_USE_TNEF** lors de l’appel de [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) pour convertir un message MAPI sortant en flux MIME peut également appliquer le TNEF. Cela s’applique même **si dispidUseTNEF n’est** pas définie. 
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Définit les structures de données de base utilisées dans les opérations distantes.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les objets de message électronique.
    
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

