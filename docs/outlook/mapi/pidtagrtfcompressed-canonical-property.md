---
title: Propriété canonique PidTagRtfCompressed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfCompressed
api_type:
- COM
ms.assetid: fd0ccb88-55ce-4d7c-9573-6e5d6239b6a8
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c88e6789b5b48e946d86a0458674a0fbe6b76356
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575447"
---
# <a name="pidtagrtfcompressed-canonical-property"></a>Propriété canonique PidTagRtfCompressed

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient la version RTF (RICH Text Format) du texte du message, généralement dans un format compressé. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RTF_COMPRESSED  <br/> |
|Identificateur :  <br/> |0x1009  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |E-mail  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient le texte du message même que la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), mais au format RTF. 
  
Texte du message au format RTF est généralement stockée dans format compressé. Toutefois, certains systèmes ne pas condenser texte mis en forme. Pour prendre en compte les, MAPI fournit la valeur de dwMagicUncompressedRTF pour un en-tête de flux identifier les RTF décompressé et l’indicateur **STORE_UNCOMPRESSED_RTF** dans **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) pour le message magasin pour indiquer qu’elle peut stocker RTF décompressé. 
  
Pour obtenir le contenu de cette propriété, appelez **OpenProperty**, puis appelez [WrapCompressedRTFStream](wrapcompressedrtfstream.md) avec l’indicateur **MAPI_READ** . Pour écrire dans cette propriété, ouvrez-le avec les indicateurs **** n’et **MAPI_CREATE** . Cela garantit que les nouvelles données remplacent complètement toutes les anciennes données et que les écritures sont exécutées en utilisant le nombre minimal de mises à jour de la banque. 
  
Banques de messages qui prennent en charge le format RTF ignorent toutes les modifications dans l’espace blanc dans le texte du message. Lorsque **PR_BODY** est stockée pour la première fois, la banque de messages également génère et stocke cette propriété. Si la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelée par la suite et **PR_BODY** a été modifié, la banque de messages appelle la fonction de [RTFSync](rtfsync.md) pour assurer la synchronisation avec la version RTF. Si seule l’espace blanc a été modifié, les propriétés restent inchangées. Ainsi, n’importe quel format RTF important mise en forme lorsque le message transite par non RTF-prenant en charge les clients et les systèmes de messagerie. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXRTFCP]](http://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)
  
> Code et décode un flux compressé dans le corps de message RTF.
    
[[MS-OXRTFEX]](http://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)
  
> Encapsule des formats de contenu supplémentaires (tels que HTML) dans la propriété body RTF des messages et pièces jointes.
    
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

