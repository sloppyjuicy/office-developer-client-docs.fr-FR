---
title: Propriété canonique PidTagSendRichInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSendRichInfo
api_type:
- COM
ms.assetid: e85fc766-197a-484f-b600-68cd28a052a2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 11d6b8cc633707512d8f4cb7447076f88dd0f74e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599437"
---
# <a name="pidtagsendrichinfo-canonical-property"></a>Propriété canonique PidTagSendRichInfo

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si le destinataire peut recevoir tout le contenu du message, y compris les objets RTF (Rich Text Format) et OLE (Object Linking and Embedding). 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SEND_RICH_INFO  <br/> |
|Identificateur :  <br/> |0x3A40  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les objets utilisateur de liste de distribution et de messagerie exposent cette propriété. 
  
Cette propriété indique si l’expéditeur considère que le destinataire est activé pour MAPI. 
  
Lorsque cette propriété est définie sur TRUE, le transport et la passerelle peuvent transmettre l’intégralité du contenu du message, y compris les objets RTF et OLE. Le fournisseur de transport et la passerelle doivent utiliser le format TNEF (Transport Neutral Encapsulation Format) pour encapsuler toutes les propriétés qui ne sont pas natives pour tous les systèmes de messagerie impliqués. 
  
Lorsque cette propriété est définie sur FALSE, le fournisseur de transport et la passerelle sont libres d’ignorer le contenu des messages que leurs clients natifs ne peuvent pas utiliser. Par exemple, lorsque les clients ne le font pas, le fournisseur de transport ne peut envoyer que du texte simple. 
  
Lorsque cette propriété n’est pas définie, le comportement par défaut est déterminé par l’implémentation du fournisseur de transport, de l’agent de transfert de messages (MTA) ou de la passerelle. Les fournisseurs de carnet d’adresses ne sont pas requis pour prendre en charge cette propriété. Par exemple, un carnet d’adresses et un fournisseur de transport étroitement couplés peuvent choisir d’envoyer le TNEF, mais ne jamais utiliser rtf. 
  
Le client ne doit pas supposer que le fournisseur de transport et la passerelle utiliseront le TNEF de leur propre initiative. Certains fournisseurs de transport et passerelles qui la transmettent au TNEF sans prendre en compte la valeur de cette propriété, mais d’autres refusent de construire ou d’envoyer le TNEF s’il n’est pas définie sur TRUE. 
  
> [!NOTE]
> La définition de cette propriété et les décisions basées sur sa valeur sont basées sur chaque destinataire. 
  
Par défaut, MAPI définit la valeur sur TRUE. Un client appelant [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) ou un fournisseur appelant [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) peut définir le bit **MAPI_SEND_NO_RICH_INFO** dans le paramètre  _ulFlags,_ ce qui entraîne mapI à définir cette propriété sur FALSE. Les one-offs créés par l’interface utilisateur utilisent la valeur spécifiée par le modèle de création. 
  
Lors des appels à la méthode [IAddrBook::ResolveName](iaddrbook-resolvename.md) lorsque le nom ne peut pas être résolu mais qu’il peut être interprété comme une adresse Internet (SMTP), cette propriété est définie sur FALSE. Pour être interprété comme une adresse Internet, le nom complet de l’entrée non résolue doit être au format X@Y. Z, par exemple « pete@pinecone.com ». 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les objets de message électronique.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> des conventions de messagerie standard Internet aux objets de message.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

