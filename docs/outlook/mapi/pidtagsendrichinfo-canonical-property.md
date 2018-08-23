---
title: Propriété canonique PidTagSendRichInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendRichInfo
api_type:
- COM
ms.assetid: e85fc766-197a-484f-b600-68cd28a052a2
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a1db4ba7a70695b17631ca13f1728043be8164bd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575965"
---
# <a name="pidtagsendrichinfo-canonical-property"></a>Propriété canonique PidTagSendRichInfo

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE si le destinataire peut recevoir le contenu du message, y compris le Format RTF (RICH Text Format) et les objets Object Linking and Embedding (OLE). 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SEND_RICH_INFO  <br/> |
|Identificateur :  <br/> |0x3A40  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que la liste de distribution et des objets utilisateur de messagerie exposent cette propriété. 
  
Cette propriété indique si l’expéditeur considère que le destinataire doit être compatible MAPI. 
  
Lorsque cette propriété est définie sur TRUE, le transport et la passerelle peuvent transmettre l’intégralité du contenu du message, y compris les objets RTF et OLE. Le fournisseur de transport et de la passerelle doivent utiliser Neutral Encapsulation Format TNEF (Transport) pour encapsuler des propriétés qui ne sont pas natives à tous les systèmes de messagerie nécessaires. 
  
Lorsque cette propriété est définie sur FALSE, le fournisseur de transport et la passerelle sont libres d’ignorer le contenu des messages que leurs clients natifs ne peut pas utiliser. Par exemple, lorsque les clients ne prennent pas en charge au format RTF, le fournisseur de transport peut envoyer uniquement du texte brut. 
  
Lorsque cette propriété n’est pas définie, le comportement par défaut est déterminé par l’implémentation du fournisseur de transport, message transfert agent d’ou de passerelle. Fournisseurs de carnet d’adresses ne sont pas nécessaire pour prendre en charge cette propriété. Par exemple, un fournisseur de transport et le carnet d’adresses étroitement couplés peut choisir d’envoyer TNEF mais jamais utiliser le format RTF. 
  
Le client ne doit pas utiliser le fournisseur de transport et passerelle utilisera TNEF sur leur propre initiative. Certains fournisseurs de transport et les passerelles qui prennent en charge TNEF transmettent, indépendamment de la valeur de cette propriété, mais d’autres personnes refuser construire ou envoyer TNEF si elle n’est pas définie sur TRUE. 
  
> [!NOTE]
> La valeur de cette propriété et les décisions en fonction de sa valeur, se trouvent sur une base par destinataire. 
  
Par défaut, MAPI définit la valeur True. Un client appelant [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) ou un fournisseur de l’appel [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) pouvez définir le bit **MAPI_SEND_NO_RICH_INFO** dans le paramètre _ulFlags_ , ce qui fait que MAPI définir cette propriété sur FALSE. Uniques créés par l’interface utilisateur utilisent la valeur spécifiée par le modèle de création. 
  
Pour les appels à la méthode [IAddrBook::ResolveName](iaddrbook-resolvename.md) lorsque le nom ne peut pas être résolu, mais peut être interprété comme une adresse Internet (SMTP), cette propriété est définie sur FALSE. Pour être interprété comme une adresse Internet, le nom complet de l’entrée non résolue doit être au format X@Y. Z, tel que « pete@pinecone.com ». 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> des conventions de messagerie standard Internet aux objets de message.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

