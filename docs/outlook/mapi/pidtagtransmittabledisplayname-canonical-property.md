---
title: Propriété canonique PidTagTransmittableDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransmittableDisplayName
api_type:
- COM
ms.assetid: aadd9086-b936-4067-bf7d-f54fc50e3c83
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 96eaf6c3f9ddc9d4bf6bc16ddc28a6f38bc311f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786880"
---
# <a name="pidtagtransmittabledisplayname-canonical-property"></a>Propriété canonique PidTagTransmittableDisplayName

  
  
**S’applique à**: Outlook 
  
Contient le nom d’affichage d’un destinataire dans un formulaire sécurisé qui ne peut pas être modifié.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W  <br/> |
|Identificateur :  <br/> |0x3A20  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Zone :  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés doivent être implémentées par tous les fournisseurs de carnet d’adresses. Elles contiennent la version du nom complet du destinataire est transmise avec le message. Pour la plupart des fournisseurs de carnet d’adresses, ces propriétés ont la même valeur que la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Fournisseurs qui n’ont pas un nom d’affichage d’informations sécurisé renvoyer des modifications PT_ERROR et MAPI le nom complet en ajoutant le nom entre guillemets.
  
Une application cliente peut utiliser cette propriété pour éviter toute altération ou « usurpation d’identité » des entrées. Un exemple d’usurpation transmet John Doe comme pré (qu’un expert).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Gère les communications d’un client avec un serveur NSPI Name Service Provider Interface ().
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

