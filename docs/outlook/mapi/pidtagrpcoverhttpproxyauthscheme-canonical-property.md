---
title: Propriété canonique PidTagRpcOverHttpProxyAuthScheme
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6da78f1a-6423-460c-b3a9-fd6441df9cef
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 91804402fd00b2671fa797113059074d4557075b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555138"
---
# <a name="pidtagrpcoverhttpproxyauthscheme-canonical-property"></a>Propriété canonique PidTagRpcOverHttpProxyAuthScheme

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente le protocole d’authentification à utiliser pour ce profil.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ROH_PROXY_AUTH_SCHEME  <br/> |
|Identificateur :  <br/> |0x6627  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Divers  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété peut être définie pour l’authentification de base ou l’authentification NT LAN Manager (NTLM). Les valeurs possibles pour cette propriété sont les valeurs ci-après.
  
|**Name**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|**ROHAUTH_BASIC** <br/> |0x1  <br/> |Authentification de base  <br/> |
|**ROHAUTH_NTLM** <br/> |0x2  <br/> |Authentification NTLM  <br/> |
   
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

