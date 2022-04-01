---
title: Propriété canonique PidTagProcessed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagProcessed
api_type:
- COM
ms.assetid: 44884f60-7e36-45b2-9712-4f9821a0dc1f
description: Définissez cette valeur sur TRUE lorsque la demande de réunion a été traitée. Cette propriété garantit que les demandes de réunion sont traitées une seule fois.
ms.openlocfilehash: 629059df7afe1a042264d21895f68ab2dec630da
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523338"
---
# <a name="pidtagprocessed-canonical-property"></a>Propriété canonique PidTagProcessed

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définissez cette valeur sur TRUE lorsque la demande de réunion a été traitée.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROCESSED  <br/> |
|Identificateur :  <br/> |0x7D01  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété garantit que les demandes de réunion sont traitées une seule fois. Le créateur de la demande doit définir cette propriété sur FALSE et le destinataire doit la définir sur TRUE une fois la demande dans le calendrier.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les objets de liste de distribution personnelle et de contact.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

