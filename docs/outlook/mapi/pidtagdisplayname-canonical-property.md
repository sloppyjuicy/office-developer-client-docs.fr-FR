---
title: Propriété canonique PidTagDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayName
api_type:
- HeaderDef
ms.assetid: bd094e00-5c60-4bb3-9a45-b943fab52876
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 834141fe3e57fde5e6404776e0ad5ce3b438450e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360801"
---
# <a name="pidtagdisplayname-canonical-property"></a>Propriété canonique PidTagDisplayName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom complet d'un objet MAPI donné. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W  <br/> |
|Identificateur :  <br/> |0x3001  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |MAPI commun  <br/> |
   
## <a name="remarks"></a>Remarques

Les dossiers ont besoin de sous-dossiers frères pour avoir des noms complets uniques. Par exemple, si un dossier contient deux sous-dossiers, les deux sous-dossiers ne peuvent pas utiliser la même valeur pour cette propriété. Cette restriction ne s'applique pas aux autres conteneurs, tels que les carnets d'adresses et les listes de distribution. 
  
Les fournisseurs de services doivent définir la valeur de cette propriété afin qu'elle contienne à la fois le type de fournisseur et les informations de configuration. Les informations supplémentaires permettent de faire la distinction entre les instances de fournisseurs du même type. Les fournisseurs non configurés doivent utiliser une chaîne qui nomme le fournisseur. Les fournisseurs configurés doivent utiliser la même chaîne suivie d'une chaîne distinctive entre parenthèses. Par exemple, un fournisseur de banque de messages non configuré peut définir ces propriétés sur: 
  
Banque d'informations personnelles
  
La version configurée peut ensuite définir ces propriétés sur: 
  
Banque d'informations personnelles (6 février 1998)
  
Pour les objets d'État, ces propriétés contiennent le nom du composant qui peut être affiché par l'interface utilisateur. 
  
> [!NOTE]
> Les points-virgules ne peuvent pas être utilisés dans les noms de destinataires de la messagerie MAPI. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelle.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les listes d'utilisateurs, de contacts, de groupes et de ressources.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> ConVertit des conventions de messagerie standard Internet en objets message.
    
[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)
  
> Étend le protocole WebDAV qui spécifie comment demander et définir le descripteur de sécurité Exchange via les méthodes WebDAV.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

