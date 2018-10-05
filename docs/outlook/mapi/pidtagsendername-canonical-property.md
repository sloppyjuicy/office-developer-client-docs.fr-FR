---
title: Propriété canonique PidTagSenderName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderName
api_type:
- COM
ms.assetid: 33fb53a8-4c7b-4418-8849-b6f9a1580172
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 953e792b6d18f7da9ee7eb17e07e6e05557e98ae
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398457"
---
# <a name="pidtagsendername-canonical-property"></a>Propriété canonique PidTagSenderName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom complet de l’expéditeur du message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SENDER_NAME, PR_SENDER_NAME_A, PR_SENDER_NAME_W  <br/> |
|Identificateur :  <br/> |0x0C1A  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Domaine :  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont des exemples de propriétés d’adresse pour l’expéditeur du message. Elle doit être définie par le fournisseur de transport sortant, qui ne doit jamais propager toutes les valeurs existantes.
  
Si aucun fournisseur de transport n’a fourni les propriétés d’adresse de l’expéditeur, le spouleur MAPI tente de les remplir en appelant la méthode [IMAPISession::QueryIdentity](imapisession-queryidentity.md) pour un identificateur d’entrée. Si aucun identificateur d’entrée n’ont été fournies, le spouleur MAPI stocke « Inconnue » dans toutes les propriétés d’adresse d’expéditeur de type PT_TSTRING. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Décrit le format des messages utilisé pour envoyer des informations relatives au partage de dossiers sur le client.
    
[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui représentent les éléments RSS.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.
    
[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour publier des objets.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.
    
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

