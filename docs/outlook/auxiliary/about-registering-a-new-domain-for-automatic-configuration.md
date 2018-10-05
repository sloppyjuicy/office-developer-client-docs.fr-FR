---
title: À propos de l’inscription d’un nouveau domaine pour la configuration automatique
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a7ab8a50-dd30-4ba5-b6d8-e6d1f482e6f1
description: Outlook permet de spécifier un nouveau domaine de service de message pour la configuration automatique et autoriser le fournisseur de service de message configurer le compte.
ms.openlocfilehash: bf06ff8d145ed6173e3545f784f8b5b7b5f433be
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388601"
---
# <a name="about-registering-a-new-domain-for-automatic-configuration"></a>À propos de l’inscription d’un nouveau domaine pour la configuration automatique

Outlook permet de spécifier un nouveau domaine de service de message pour la configuration automatique et autoriser le fournisseur de service de message configurer le compte.
  
Lorsque vous créez un fournisseur de service de message, vous pouvez utiliser la clé suivante dans le Registre Windows pour spécifier un nouveau domaine sera automatiquement configuré par le fournisseur de service de message correspondant : 
  
`HKLM\Software\Microsoft\Office\Outlook\AutoConfigDomains\<domain name>\`
  
Dans la clé `<domain name>` est le domaine pour la configuration automatique. Ce nom de domaine prend en charge un caractère générique \* au début uniquement. Le tableau suivant présente les valeurs que cette clé prend en charge. 
  
| Valeur | Type | Description |
|:-----|:-----|:-----|
|Nom convivial  <br/> |REG_SZ  <br/> |Le nom de domaine qui s’affiche à l’utilisateur pendant la configuration automatique.  <br/> |
|Nom de service  <br/> |REG_SZ  <br/> |Le service de message enregistré dans mapisvc.inf qui prend en charge ce domaine.  <br/> |
|Emplacement d’installation  <br/> |REG_SZ  <br/> |L’URL de l’emplacement pour installer le fournisseur de service de message, s’il n’est pas déjà installé.  <br/> |
|Version minimum  <br/> |REG_DWORD  <br/> |La version minimale de la DLL du fournisseur de services de message est nécessaire. Cette valeur est facultative.  <br/> |
   
Lorsque Outlook commence la configuration automatique pour un compte de messagerie, il vérifie le Registre Windows pour l’inscription du domaine spécifié par l’adresse de messagerie. Si le domaine est déjà spécifié dans le Registre Windows, Outlook vérifie si le service de message est enregistré dans le fichier Mapisvc.inf. Outlook ne peut pas continuer avec la configuration automatique du domaine, sauf si elle a été spécifié dans le Registre Windows.
  
Si le service de message spécifié n’est pas actuellement enregistré dans Mapisvc.inf, ou le fournisseur de service de message est installé, mais le fichier .dll dispose d’une version antérieure à la valeur minimale spécifiée, Outlook utilise le nom convivial spécifié et invite l’utilisateur à installer le fournisseur de services. Si l’utilisateur accepte, Outlook redirige l’utilisateur vers l’emplacement d’installation spécifié afin que l’utilisateur peut installer le fournisseur. L’installation du fournisseur inscrit le service dans le fichier Mapisvc.inf.
  
Si le message service est actuellement inscrit dans Mapisvc.inf et la DLL de fournisseur de service est une version appropriée, Outlook crée le service de message à l’aide de [IMsgServiceAdmin::CreateMsgService](https://msdn.microsoft.com/library/0135f049-0311-45e5-9685-78597d599a4e%28Office.15%29.aspx)et il configure ensuite à l’aide de [ IMsgServiceAdmin::ConfigureMsgService](https://msdn.microsoft.com/library/a08f5905-2585-49ca-abb7-a77f2736f604%28Office.15%29.aspx). Configuration automatique d’Outlook utilise les trois propriétés suivantes pour autoriser le fournisseur à configurer le compte : [PidTagAutoConfigurationUserName](https://msdn.microsoft.com/library/05dfa0e2-4ab1-4f57-9009-6a815aca87bd%28Office.15%29.aspx), [PidTagAutoConfigurationUserEmail](https://msdn.microsoft.com/library/845140c8-5454-4b47-acec-ab5aff00b768%28Office.15%29.aspx)et [PidTagAutoConfigurationUserPassword ](https://msdn.microsoft.com/library/d33e7c45-55d8-4dc1-ade9-605542d87e61%28Office.15%29.aspx).
  
## <a name="see-also"></a>Voir aussi

- [Format de fichier de MapiSvc.inf](https://msdn.microsoft.com/library/b48eda17-83a8-4dc4-85c8-4ca827d13d25%28Office.15%29.aspx)

