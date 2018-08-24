---
title: Propriété canonique PidTagRpcOverHttpFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b36f71958528b25829b1ff85b29572b3590f9d4f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594816"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a>Propriété canonique PidTagRpcOverHttpFlags

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient les paramètres d’un profil utilisé par Microsoft Office Outlook pour se connecter à Microsoft Exchange Server à l’aide d’un appel de procédure distante (RPC) sur protocole HTTP (Hypertext Transfer).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ROH_FLAGS  <br/> |
|Identificateur :  <br/> |0x6623  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

La propriété **PR_ROH_FLAGS** est stockée dans la Section profil globale d’un profil MAPI Messaging Application Programming Interface (). La valeur de **PR_ROH_FLAGS** est un masque de bits qui est composée d’un ou plusieurs des indicateurs suivants. 
  
|**Nom**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**ROHFLAGS_USE_ROH** <br/> |0 x 1  <br/> |Connectez-vous au serveur Exchange en utilisant RPC sur HTTP.  <br/> |
|**ROHFLAGS_SSL_ONLY** <br/> |0 x 2  <br/> |Connectez-vous au serveur Exchange à l’aide de Secure Sockets Layer (SSL) uniquement.  <br/> |
|**ROHFLAGS_MUTUAL_AUTH** <br/> |0 x 4  <br/> |Authentifier mutuellement la session lors de la connexion à l’aide de SSL.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_FAST** <br/> |0 x 8  <br/> |Sur des réseaux rapides, se connecter via le protocole HTTP. Ensuite, connectez-vous à l’aide de TCP/IP.  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_SLOW** <br/> |0 x 20  <br/> |Sur des réseaux lents, se connecter via le protocole HTTP. Ensuite, connectez-vous à l’aide de TCP/IP.  <br/> |
   
Par exemple, pour définir le **PR_ROH_FLAGS** propriété pour activer RPC sur HTTP, pour exiger le chiffrement SSL et pour indiquer que le protocole HTTP doit être utilisé tout d’abord sur Mes connexions lentes, définie la valeur de la propriété **PR_ROH_FLAGS** à `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` qui est égal à 0 x 23. 
  
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
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

