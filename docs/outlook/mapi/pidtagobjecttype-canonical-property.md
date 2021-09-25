---
title: Propriété canonique PidTagObjectType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagObjectType
api_type:
- HeaderDef
ms.assetid: 37da4ff5-300d-479f-a8b4-6fc36df997d9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e23518b68d204982511ccf492d09d2cd310380ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560808"
---
# <a name="pidtagobjecttype-canonical-property"></a>Propriété canonique PidTagObjectType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le type d’un objet. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_OBJECT_TYPE  <br/> |
|Identificateur :  <br/> |0x0FFE  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Courant  <br/> |
   
## <a name="remarks"></a>Remarques

Le type d’objet contenu dans cette propriété correspond à l’interface principale disponible pour un objet accessible via l’interface **OpenEntry.** Elle est généralement obtenue en consultant le  _paramètre lpulObjType_ renvoyé par la méthode **OpenEntry** appropriée. Lorsque l’interface est obtenue d’autres manières, appelez [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur de cette propriété. 
  
Cette propriété peut avoir exactement l’une des valeurs suivantes :
  
MAPI_ABCONT 
  
> Objet conteneur de carnet d’adresses 
    
MAPI_ADDRBOOK 
  
> Objet carnet d’adresses 
    
MAPI_ATTACH 
  
> Objet de pièce jointe de message 
    
MAPI_DISTLIST 
  
> Objet de liste de distribution 
    
MAPI_FOLDER 
  
> Objet de dossier 
    
MAPI_FORMINFO 
  
> Objet Form 
    
MAPI_MAILUSER 
  
> Objet utilisateur de messagerie 
    
MAPI_MESSAGE 
  
> Message, objet 
    
MAPI_PROFSECT 
  
> Objet section profil 
    
MAPI_SESSION 
  
> Objet Session 
    
MAPI_STATUS 
  
> Objet Status 
    
MAPI_STORE 
  
> Objet de la boutique de messages
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Gère les communications d’un client avec un serveur NSPI (Name Service Provider Interface).
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l’ordre et le flux des transferts de données entre un client et un serveur.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet en objets de message.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
[[MS-OXOAB]](https://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)
  
> Spécifie les formats de fichier de carnet d’adresses en mode hors connexion pour le cache d’objets du carnet d’adresses local.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les objets de message électronique.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations de manipulation d’une configuration de liste de dossiers de recherche.
    
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

