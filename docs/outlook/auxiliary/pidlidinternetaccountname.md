---
title: PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5acca047-ff2a-716c-8dd4-b676fce1a3cf
description: Renvoie le nom complet du compte remis le message.
ms.openlocfilehash: 223bc5bbd485426676376d94875274613ff59685
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782808"
---
# <a name="pidlidinternetaccountname"></a>PidLidInternetAccountName

Renvoie le nom complet du compte remis le message.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidInetAcctName  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID de type long (capot) :  <br/> |0x00008580  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Zone :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété doit contenir la même valeur que celle qui est renvoyée par la propriété API de gestion de compte [PROP_ACCT_NAME](prop_acct_name.md) pour le compte remis le message. 
  
Fournisseurs de banque de messages exposent cette propriété nommée et les [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md) afin que les actions suivantes se produisent : 
  
- Lorsqu’un utilisateur clique sur **répondre à tous** dans un message électronique, Outlook supprime l’adresse de messagerie qui est associée au compte et est marqué sur le message à partir de la liste des destinataires de la réponse. Ce problème se produit, sauf si cette adresse de messagerie est l’expéditeur du message d’origine. 
    
- Par défaut, Outlook envoie les réponses et les transferts par le biais du compte qui est marqué sur le message d’origine.
    
En règle générale, le Gestionnaire de protocole Outlook remet des messages et Outlook définit les propriétés **PidLidInternetAccountName** et **PidLidInternetAccountStamp** pour indiquer le compte qui remis le message. Toutefois, si une banque de messages fortement couplée à un type de transport, le Gestionnaire de protocole Outlook ne fournit pas les messages et Outlook ne peut pas définir ces propriétés. Dans ce scénario, Outlook appelle la fonction [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) . Si le fournisseur de banque de messages souhaite exposer ces propriétés nommées, il doit implémenter **IMAPIProp::GetIDsFromNames** et renvoyer les balises de propriété via le paramètre de sortie *lppPropTags* . Outlook peut puis appelez la méthode [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) à l’aide de ces balises de propriété, et le fournisseur de banque de message peut renvoyer le nom de compte et le cachet du compte désiré. 
  
Pour prendre en charge ces propriétés nommées, les fournisseurs de magasins doivent attends qu’Outlook **IMAPIProp::GetIDsFromNames** permet d’obtenir la balise de propriété pour cette propriété. Outlook spécifie les valeurs suivantes pour la structure [MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) qui correspond à cette propriété nommée, qui est passée en tant que partie de la batterie sur laquelle pointée le paramètre d’entrée *lppPropNames* de **IMAPIProp::GetIDsFromNames**. 
  
|||
|:-----|:-----|
|lpGuid :  <br/> |PSETID_Common  <br/> |
|ulKind :  <br/> |MNID_ID  <br/> |
|Kind.lID :  <br/> |dispidInetAcctName  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [À propos de l'API de gestion de compte](about-the-account-management-api.md)
- [Constantes (API de gestion des comptes)](constants-account-management-api.md)
- [Propriété canonique PidLidInternetAccountName](http://msdn.microsoft.com/library/29bedadf-903d-419d-804d-dc8bd92b745d%28Office.15%29.aspx)

