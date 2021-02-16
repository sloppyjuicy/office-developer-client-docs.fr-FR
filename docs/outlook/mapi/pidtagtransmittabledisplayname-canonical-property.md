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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e66fe8d3621c122ccc19bdde169f20f7d47a148d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331856"
---
# <a name="pidtagtransmittabledisplayname-canonical-property"></a>Propriété canonique PidTagTransmittableDisplayName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom complet d’un destinataire dans un formulaire sécurisé qui ne peut pas être modifié.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W  <br/> |
|Identificateur :  <br/> |0x3A20  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Domaine :  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés doivent être implémentées par tous les fournisseurs de carnets d’adresses. Ils contiennent la version du nom complet du destinataire qui est transmise avec le message. Pour la plupart des fournisseurs de carnet d’adresses, ces propriétés ont la même valeur que **la propriété PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Les fournisseurs qui n’ont pas de nom d’affichage sécurisé PT_ERROR et MAPI modifie le nom complet en ajoutant des guillemets autour du nom.
  
Une application cliente peut utiliser cette propriété pour empêcher l’altération ou l’usurpation d’entrées. Un exemple d’usurpation est la transmission de John Doe en tant que John (What a Guy) Doe.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server de protocole associées.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Gère les communications d’un client avec un serveur NSPI (Name Service Provider Interface).
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l’ordre et le flux des transferts de données entre un client et un serveur.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
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

