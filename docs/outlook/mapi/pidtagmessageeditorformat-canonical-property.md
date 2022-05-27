---
title: Propriété canonique PidTagMessageEditorFormat
description: Décrit la propriété canonique PidTagMessageEditorFormat, qui spécifie le format d’un éditeur à utiliser pour afficher un message.
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
ms.openlocfilehash: ddf0f46c26a7e1e17e5384a30872588cb52b60fd
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752273"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a>Propriété canonique PidTagMessageEditorFormat

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie le format d’un éditeur à utiliser pour afficher un message.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MSG_EDITOR_FORMAT  <br/> |
|Identificateur :  <br/> |0x5909  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs possibles pour **PR_MSG_EDITOR_FORMAT** peuvent être l’une des suivantes : 
  
|**Valeur**|**Description**|
|:-----|:-----|
|**EDITOR_FORMAT_DONTKNOW** <br/> |Le format de l’éditeur à utiliser est inconnu. |
|**EDITOR_FORMAT_PLAINTEXT** <br/> |L’éditeur doit afficher le message au format texte brut. |
|**EDITOR_FORMAT_HTML** <br/> |L’éditeur doit afficher le message au format HTML. |
|**EDITOR_FORMAT_RTF** <br/> |L’éditeur doit afficher le message au format texte enrichi. |
   
Par défaut, les messages électroniques (avec la classe **de message IPM. Remarque** ou avec une classe de message personnalisée dérivée **d’IPM. Remarque**) Les messages envoyés à partir d’un compte de messagerie POP3/SMTP sont envoyés au format TNEF (Transport Neutral Encapsulation Format). La propriété **PR_MSG_EDITOR_FORMAT** peut être utilisée pour appliquer uniquement du texte brut, et non TNEF, lors de l’envoi d’un message. Si **PR_MSG_EDITOR_FORMAT** est défini sur **EDITOR_FORMAT_PLAINTEXT**, le message est envoyé en texte brut sans TNEF. Si **PR_MSG_EDITOR_FORMAT** est défini sur **EDITOR_FORMAT_RTF**, l’encodage TNEF est implicitement activé et le message est envoyé à l’aide du format Internet par défaut spécifié dans le client Outlook.
  
Il existe deux autres façons d’appliquer l’utilisation de TNEF lors de l’envoi d’un message.
  
- La définition de la propriété nommée **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) sur True sur un message indique que TNEF doit être inclus lors de la conversion du message de MAPI en MIME/SMTP. Notez que **dispidUseTNEF** s’applique uniquement lorsque le message est envoyé à partir d’un compte de messagerie POP3/SMTP et ne s’applique pas lorsque le message est envoyé par d’autres fournisseurs, tels que Microsoft Exchange Server. **dispidUseTNEF** remplace le paramètre dans **PR_MSG_EDITOR_FORMAT**.
    
- L’utilisation de l’indicateur **CCSF_USE_TNEF** lors de l’appel [d’IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) pour convertir un message MAPI sortant en flux MIME peut également appliquer TNEF. Cela s’applique même si **dispidUseTNEF** n’est pas défini. 
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Définit les structures de données de base utilisées dans les opérations à distance.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les objets de courrier électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

