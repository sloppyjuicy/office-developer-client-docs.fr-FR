---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: Renvoie le cachet du compte qui a remis le message.
ms.openlocfilehash: aa81ce920cc448557bc23a0ba0fde603934f8e39
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572227"
---
# <a name="pidlidinternetaccountstamp"></a>PidLidInternetAccountStamp

Renvoie le cachet du compte qui a remis le message.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidInetAcctStamp  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x00008581  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit contenir la même valeur que celle renvoyée par la propriété API de gestion des [PROP_ACCT_STAMP](prop_acct_stamp.md) du compte qui a remis le message. 
  
Les fournisseurs de magasins de messages exposent cette propriété nommée et [PidLidInternetAccountName](pidlidinternetaccountname.md) afin que les actions suivantes se produisent : 
  
- Lorsqu’un utilisateur  clique sur Répondre à tous dans un message électronique, Outlook supprime l’adresse de messagerie associée au compte et est inscrite sur le message dans la liste des destinataires de la réponse. Ce comportement se produit sauf si cette adresse de messagerie est l’expéditeur du message d’origine. 
    
- Par défaut, Outlook envoie des réponses et des messages transmis via le compte qui est marqué sur le message d’origine.
    
Généralement, le gestionnaire de protocole Outlook fournit des messages et Outlook définit les propriétés **PidLidInternetAccountName** et **PidLidInternetAccountStamp** pour indiquer le compte qui a remis le message. Toutefois, si un magasin de messages est étroitement associé à un transport, le gestionnaire de protocole Outlook ne fournit pas de messages et Outlook ne peut pas définir ces propriétés. Dans ce scénario, Outlook la [fonction IMAPIProp::GetIDsFromNames.](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) Si le fournisseur de magasin de messages souhaite exposer ces propriétés nommées, il doit implémenter **IMAPIProp::GetIDsFromNames** et renvoyer des balises de propriété via le paramètre de sortie  *lppPropTags*  . Outlook pouvez ensuite appeler la méthode [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) à l’aide de ces balises de propriété, et le fournisseur de banque de messages peut renvoyer le nom de compte et le cachet du compte souhaité. 
  
Pour prendre en charge ces propriétés nommées, les fournisseurs de magasins doivent s’attendre à ce que Outlook utilise **IMAPIProp::GetIDsFromNames** pour obtenir la balise de propriété pour cette propriété. Outlook spécifie les valeurs suivantes pour la structure [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) qui correspond à cette propriété nommée, qui est passée dans le cadre du tableau pointé par le paramètre d’entrée *lppPropNames of* **IMAPIProp::GetIDsFromNames**. 
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind :  <br/> |MNID_ID  <br/> |
|Kind.lID :  <br/> |dispidInetAcctStamp  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)
- [Propriété canonique PidLidInternetAccountStamp](https://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

