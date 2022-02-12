---
title: Propriété canonique PidTagRpcOverHttpFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1760a24e1e4a8b742934ec0ffd3a0d7a570baa67
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62787687"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a>Propriété canonique PidTagRpcOverHttpFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient les paramètres d’un profil utilisé par Microsoft Office Outlook pour se connecter à Microsoft Exchange Server à l’aide d’un appel de procédure distante (RPC) sur HTTP (Hypertext Transfer Protocol).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ROH_FLAGS  <br/> |
|Identificateur :  <br/> |0x6623  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

La **PR_ROH_FLAGS** est stockée dans la section Profil global d’un profil MAPI (Messaging Application Programming Interface). La valeur de **PR_ROH_FLAGS** est un masque de bits composé d’un ou plusieurs des indicateurs suivants. 
  
|**Name**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**ROHFLAGS_USE_ROH** <br/> |0x1  <br/> |Connecter au Exchange Server l’aide de RPC sur HTTP. |
|**ROHFLAGS_SSL_ONLY** <br/> |0x2  <br/> |Connecter au Exchange Server à l’aide du SSL (Secure Socket Layer) uniquement. |
|**ROHFLAGS_MUTUAL_AUTH** <br/> |0x4  <br/> |Authentifier mutuellement la session lors de la connexion à l’aide de SSL. |
|**ROHFLAGS_HTTP_FIRST_ON_FAST** <br/> |0x8  <br/> |Sur les réseaux rapides, connectez-vous d’abord à l’aide du protocole HTTP. Ensuite, connectez-vous à l’aide de TCP/IP. |
|**ROHFLAGS_HTTP_FIRST_ON_SLOW** <br/> |0x20  <br/> |Sur les réseaux lents, connectez-vous d’abord à l’aide du protocole HTTP. Ensuite, connectez-vous à l’aide de TCP/IP. |
   
Par exemple, pour définir la propriété **PR_ROH_FLAGS** pour activer RPC sur HTTP, pour exiger SSL et pour spécifier que le protocole HTTP doit être utilisé en premier sur les connexions lentes, définissez la valeur de la propriété **PR_ROH_FLAGS**  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` égale à 0x23. 
  
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

