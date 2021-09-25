---
title: À propos de l’inscription d’un nouveau domaine pour la configuration automatique
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: a7ab8a50-dd30-4ba5-b6d8-e6d1f482e6f1
description: Outlook permet de spécifier un nouveau domaine de service de messagerie pour la configuration automatique et d’autoriser le fournisseur de services de messagerie à configurer le compte.
ms.openlocfilehash: c038bf3461a3452b692687b1a2f6f541c2e45092
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572241"
---
# <a name="about-registering-a-new-domain-for-automatic-configuration"></a>À propos de l’inscription d’un nouveau domaine pour la configuration automatique

Outlook permet de spécifier un nouveau domaine de service de messagerie pour la configuration automatique et d’autoriser le fournisseur de services de messagerie à configurer le compte.
  
Lors de la conception d’un fournisseur de services de messagerie, vous pouvez utiliser la clé suivante dans le Registre Windows pour spécifier un nouveau domaine à configurer automatiquement par le fournisseur de services de messagerie correspondant : 
  
`HKLM\Software\Microsoft\Office\Outlook\AutoConfigDomains\<domain name>\`
  
Dans la clé, `<domain name>` est le domaine pour la configuration automatique. Ce nom de domaine prend en charge un caractère \* générique au début uniquement. Le tableau suivant indique les valeurs que cette clé prend en charge. 
  
| Valeur | Type | Description |
|:-----|:-----|:-----|
|Nom convivial  <br/> |REG_SZ  <br/> |Nom de domaine affiché à l’utilisateur lors de la configuration automatique.  <br/> |
|Nom du service  <br/> |REG_SZ  <br/> |Service de message enregistré dans mapisvc.inf qui prend en charge ce domaine.  <br/> |
|Emplacement d’installation  <br/> |REG_SZ  <br/> |URL de l’emplacement où installer le fournisseur de services de messagerie, s’il n’est pas déjà installé.  <br/> |
|Version minimale  <br/> |REG_DWORD  <br/> |Version minimale de l'.dll du fournisseur de services de messagerie requis. Cette valeur est facultative.  <br/> |
   
Lorsque Outlook commence la configuration automatique d’un compte de messagerie, il vérifie le registre Windows pour l’inscription du domaine spécifié par l’adresse e-mail. Si le domaine est déjà spécifié dans le Registre Windows, Outlook si le service de message est inscrit dans Mapisvc.inf. Outlook ne peut pas procéder à la configuration automatique du domaine, sauf si elle a été spécifiée dans Windows registre.
  
Si le service de messagerie spécifié n’est pas actuellement inscrit dans Mapisvc.inf ou si le fournisseur de services de messagerie est installé mais que la version du .dll est antérieure à la version minimale spécifiée, Outlook utilise le nom convivial spécifié et invite l’utilisateur à installer le fournisseur. Si l’utilisateur l’accepte, Outlook redirige l’utilisateur vers l’emplacement d’installation spécifié afin que l’utilisateur puisse installer le fournisseur. L’installation du fournisseur inscrit le service de messagerie dans Mapisvc.inf.
  
Si le service de messagerie est actuellement inscrit dans Mapisvc.inf et que le fournisseur de services .dll est une version appropriée, Outlook crée le service de messagerie à l’aide de [IMsgServiceAdmin::CreateMsgService](https://msdn.microsoft.com/library/0135f049-0311-45e5-9685-78597d599a4e%28Office.15%29.aspx), puis le configure à l’aide de [IMsgServiceAdmin::ConfigureMsgService](https://msdn.microsoft.com/library/a08f5905-2585-49ca-abb7-a77f2736f604%28Office.15%29.aspx). Outlook configuration automatique utilise les trois propriétés suivantes pour permettre au fournisseur de configurer le compte : [PidTagAutoConfigurationUserName](https://msdn.microsoft.com/library/05dfa0e2-4ab1-4f57-9009-6a815aca87bd%28Office.15%29.aspx), [PidTagAutoConfigurationUserEmail](https://msdn.microsoft.com/library/845140c8-5454-4b47-acec-ab5aff00b768%28Office.15%29.aspx)et [PidTagAutoConfigurationUserPassword](https://msdn.microsoft.com/library/d33e7c45-55d8-4dc1-ade9-605542d87e61%28Office.15%29.aspx).
  
## <a name="see-also"></a>Voir aussi

- [Format de fichier de MapiSvc.inf](https://msdn.microsoft.com/library/b48eda17-83a8-4dc4-85c8-4ca827d13d25%28Office.15%29.aspx)

