---
title: Propriété canonique PidTagAccount
description: Décrit la propriété canonique PidTagAccount, qui contient le nom du compte du destinataire et s’applique à Outlook 2013 et 2016.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAccount
api_type:
- HeaderDef
ms.assetid: bec199b5-abfd-4686-ad59-21092212e1a5
ms.openlocfilehash: cb8c5ce7c1147b19eb01cf71f1d65f68c017c535
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812529"
---
# <a name="pidtagaccount-canonical-property"></a>Propriété canonique PidTagAccount

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom du compte du destinataire. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W  <br/> |
|Identificateur :  <br/> |0x3A00  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés fournissent des informations d’identification et d’accès pour un destinataire. Elles sont définies par le destinataire et son organisation.
  
Ces propriétés contiennent généralement le nom de messagerie du destinataire, c’est-à-dire le composant final de l’adresse e-mail, qui identifie de façon unique le destinataire dans l’organisation locale. Le nom de l’e-mail correspond au nom unique X.400, qui est destiné à être un nom court garanti unique au sein d’un domaine de messagerie spécifique.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les contacts et les listes de distribution personnelles.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les listes d’utilisateurs, de contacts, de groupes et de ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[IMailUser : IMAPIProp](imailuserimapiprop.md)


[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

