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
ms.openlocfilehash: a6a3eb88377777a3d27687179bfdcb82057be3a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786234"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a>Propriété canonique PidTagMessageEditorFormat

  
  
**S’applique à**: Outlook 
  
Spécifie le format d’un éditeur à utiliser pour afficher un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MSG_EDITOR_FORMAT  <br/> |
|Identificateur :  <br/> |0x5909  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs possibles de **PR_MSG_EDITOR_FORMAT** peuvent être une des options suivantes : 
  
|**Valeur**|**Description**|
|:-----|:-----|
|**EDITOR_FORMAT_DONTKNOW** <br/> |Le format de l’éditeur à utiliser est inconnu.  <br/> |
|**EDITOR_FORMAT_PLAINTEXT** <br/> |L’éditeur doit afficher le message au format texte brut.  <br/> |
|**EDITOR_FORMAT_HTML** <br/> |L’éditeur doit afficher le message au format HTML.  <br/> |
|**EDITOR_FORMAT_RTF** <br/> |L’éditeur doit afficher le message au Format RTF.  <br/> |
   
Par défaut, envoyer des messages (avec la classe de message **IPM. Remarque** ou avec une classe de message dérivée de **IPM. Notez**) envoyés à partir d’une messagerie POP3/SMTP compte sont envoyés dans le Neutral Encapsulation Format TNEF (Transport). La propriété **PR_MSG_EDITOR_FORMAT** peut être utilisée pour appliquer uniquement du texte brut et pas TNEF, lors de l’envoi d’un message. Si **PR_MSG_EDITOR_FORMAT** est défini sur **EDITOR_FORMAT_PLAINTEXT**, le message est envoyé en texte brut sans TNEF. Si **PR_MSG_EDITOR_FORMAT** est défini sur **EDITOR_FORMAT_RTF**, le codage TNEF est implicitement activé et le message est envoyé en utilisant le format Internet par défaut qui est spécifié dans le client Outlook.
  
Il existe deux autres façons d’imposer l’utilisation du format TNEF lors de l’envoi d’un message.
  
- Définition de la **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) nommé propriété la valeur True sur un message indique TNEF doit être inclus lors de la conversion du message de MAPI à MIME/SMTP. Notez que **dispidUseTNEF** s’applique uniquement lorsque le message est envoyé à partir d’un compte de messagerie POP3/SMTP et ne s’applique pas lorsque le message est envoyé par d’autres fournisseurs, tels que Microsoft Exchange Server. **dispidUseTNEF** remplace le paramètre de **PR_MSG_EDITOR_FORMAT**.
    
- À l’aide de l’indicateur **CCSF_USE_TNEF** lors de l’appel [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) pour convertir un message MAPI sortant à un flux MIME peut également appliquer TNEF. Cela s’applique même si **dispidUseTNEF** n’est pas défini. 
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Définit les structures de base de données qui sont utilisés dans les opérations à distance.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

