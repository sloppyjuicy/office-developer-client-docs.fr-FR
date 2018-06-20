---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: Renvoie le tampon de compte du compte que remis le message.
ms.openlocfilehash: ba54bffb60a05a3b4a1ff30519960740af93ebd3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782798"
---
# <a name="pidlidinternetaccountstamp"></a>PidLidInternetAccountStamp

Renvoie le tampon de compte du compte que remis le message.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidInetAcctStamp  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID de type long (capot) :  <br/> |0x00008581  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Zone :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit contenir la même valeur que celle qui est renvoyée par la propriété API de gestion de compte [PROP_ACCT_STAMP](prop_acct_stamp.md) pour le compte remis le message. 
  
Fournisseurs de banque de messages exposent cette propriété nommée et les [PidLidInternetAccountName](pidlidinternetaccountname.md) afin que les actions suivantes se produisent : 
  
- Lorsqu’un utilisateur clique sur **répondre à tous** dans un message électronique, Outlook supprime l’adresse de messagerie qui est associée au compte et est marqué sur le message à partir de la liste des destinataires de la réponse. Ce problème se produit, sauf si cette adresse de messagerie est l’expéditeur du message d’origine. 
    
- Par défaut, Outlook envoie les réponses et les transferts par le biais du compte qui est marqué sur le message d’origine.
    
En règle générale, le Gestionnaire de protocole Outlook remet des messages et Outlook définit les propriétés **PidLidInternetAccountName** et **PidLidInternetAccountStamp** pour indiquer le compte qui remis le message. Toutefois, si une banque de messages fortement couplée à un type de transport, le Gestionnaire de protocole Outlook ne fournit pas les messages et Outlook ne peut pas définir ces propriétés. Dans ce scénario, Outlook appelle la fonction [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) . Si le fournisseur de banque de messages souhaite exposer ces propriétés nommées, il doit implémenter **IMAPIProp::GetIDsFromNames** et renvoyer les balises de propriété via le paramètre de sortie *lppPropTags* . Outlook peut puis appelez la méthode [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) à l’aide de ces balises de propriété, et le fournisseur de banque de message peut renvoyer le nom de compte et le cachet du compte désiré. 
  
Pour prendre en charge ces propriétés nommées, les fournisseurs de magasins doivent attends qu’Outlook **IMAPIProp::GetIDsFromNames** permet d’obtenir la balise de propriété pour cette propriété. Outlook spécifie les valeurs suivantes pour la structure [MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) qui correspond à cette propriété nommée, qui est passée en tant que partie de la batterie sur laquelle pointée le paramètre d’entrée *lppPropNames* de **IMAPIProp::GetIDsFromNames**. 
  
|||
|:-----|:-----|
|lpGuid :  <br/> |PSETID_Common  <br/> |
|ulKind :  <br/> |MNID_ID  <br/> |
|Kind.lID :  <br/> |dispidInetAcctStamp  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md) 
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)
- [Propriété canonique PidLidInternetAccountStamp](http://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

