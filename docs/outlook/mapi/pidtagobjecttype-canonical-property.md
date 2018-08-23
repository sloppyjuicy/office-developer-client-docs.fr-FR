---
title: Propriété canonique PidTagObjectType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagObjectType
api_type:
- HeaderDef
ms.assetid: 37da4ff5-300d-479f-a8b4-6fc36df997d9
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8b2d435e132bf453cf41ec141d5a946bf54f9c66
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591050"
---
# <a name="pidtagobjecttype-canonical-property"></a>Propriété canonique PidTagObjectType

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient le type d’un objet. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_OBJECT_TYPE  <br/> |
|Identificateur :  <br/> |0x0FFE  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Common  <br/> |
   
## <a name="remarks"></a>Remarques

Le type d’objet contenu dans cette propriété correspond à l’interface principale disponible pour un objet accessible par le biais de l’interface **OpenEntry** . Il est généralement obtenue en consultant le paramètre _lpulObjType_ renvoyé par la méthode **OpenEntry** appropriée. Lorsque l’interface est obtenue par d’autres moyens, appelez [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur de cette propriété. 
  
Cette propriété peut avoir exactement une des valeurs suivantes :
  
MAPI_ABCONT 
  
> Objet conteneur de carnet d’adresses 
    
MAPI_ADDRBOOK 
  
> Objet Carnet d’adresses 
    
MAPI_ATTACH 
  
> Objet attachment de message 
    
MAPI_DISTLIST 
  
> Objet liste de distribution 
    
MAPI_FOLDER 
  
> Objet Folder 
    
MAPI_FORMINFO 
  
> Objet de formulaire 
    
MAPI_MAILUSER 
  
> Messagerie user, objet 
    
MAPI_MESSAGE 
  
> Message, objet 
    
MAPI_PROFSECT 
  
> Objet de section de profil 
    
MAPI_SESSION 
  
> Objet de la session 
    
MAPI_STATUS 
  
> Objet d’état 
    
MAPI_STORE 
  
> Objet store de message
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Gère les communications d’un client avec un serveur NSPI Name Service Provider Interface ().
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet aux objets de message.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXOAB]](http://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)
  
> Spécifie les formats de fichiers de carnet en mode hors connexion pour le cache d’objets de livre adresse locale.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.
    
[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour la manipulation d’une configuration de liste de dossier de recherche.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

