---
title: Implémentation d’un objet d’état
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 48fd3e28-c2d2-474d-9487-5e2f08ca7319
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e97efb70716ffbd7fa98f980ce8520cfcb988532
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336336"
---
# <a name="status-object-implementation"></a>Implémentation d’un objet d’état

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tous les fournisseurs de services doivent implémenter un objet d’état et en fournir les propriétés dans la table d’état de session. Vous pouvez inclure une ou plusieurs lignes dans la table d’état, selon le nombre de ressources que vous contrôlez. Un fournisseur de transport, par exemple, doit créer une ligne dans la table d’état pour chaque file d’attente de messages qu’il gère. Lorsque des modifications se produisent, la ligne de tableau d’état appropriée doit être mise à jour. Les objets d’état sont implémentés pour fournir l’accès aux informations incluses dans la table d’état et aux informations supplémentaires non incluses dans le tableau.
  
### <a name="to-implement-a-status-object"></a>Pour implémenter un objet d’état

1. Implémentez **la méthode OpenStatusEntry** de votre objet d’ouverture de connecté. Lorsque les clients souhaitent ouvrir votre objet d’état, ils appellent [IMAPISession::OpenEntry](imapisession-openentry.md). MAPI remplit la demande d’ouverture en appelant la méthode **OpenStatusEntry** de votre fournisseur, ce qui a pour effet que votre fournisseur ouvre son objet d’état et retourne au client un pointeur vers son implémentation **IMAPIStatus.** Dans votre **implémentation OpenStatusEntry,** complétez les étapes suivantes : 
    
   1. Effectuez les tâches suivantes si votre objet d’logo n’a pas encore créé d’objet d’état :
    
      1. Appelez la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) de l’objet de support pour accéder à la section de profil de votre fournisseur. 
          
      2. Créez un objet d’état.
          
      3. Stockez une référence à la section de profil dans l’objet d’état de votre fournisseur et appelez la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) de la section de profil pour incrémenter son nombre de références. 
          
      4. Stockez une référence à l’objet d’ouverture de conférence dans l’objet d’état de votre fournisseur et appelez la méthode **IUnknown::AddRef** de l’objet d’ouverture de conférence pour incrémenter son nombre de références. 
          
      5. Stockez une référence à l’objet d’état dans l’objet d’ouverture de connecté de votre fournisseur.
    
   2. Appelez la méthode **IUnknown::AddRef** de l’objet d’état pour incrémenter son nombre de références dans l’objet d’logon. 
    
   3. Définissez la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) de l’objet d’état MAPI_STATUS.
    
   4. Définissez le paramètre de sortie  _lppMAPIStatus_ pour pointer vers l’objet d’état et renvoyer. 
    
   5. Vérifiez le _paramètre d’entrée ulFlags._ Si elle est définie sur MAPI_MODIFY et que votre fournisseur prend en charge l’accès en lecture/écriture à son objet d’état, renvoyez un objet accessible en écriture. Toutefois, si votre fournisseur ne prend pas en charge l’accès en lecture/écriture à son objet d’état, ne pas échouer. Renvoyer un objet d’état en lecture seule. Les clients qui s’attendent à recevoir des objets d’état de lecture/écriture doivent vérifier que l’autorisation de lecture/écriture a été accordée avant d’essayer d’apporter des modifications. 
    
2. Définissez toutes les propriétés d’objet d’état et de table d’état requises. Les propriétés que vous incluez dans la ligne de votre tableau d’état doivent être disponibles via votre objet d’état, à l’exception des propriétés calculées par MAPI. Les propriétés requises sont les suivantes :
    
   - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   - **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))
    
   - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   - **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))
    
   - **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
    
   - **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))
    
   - **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))
    
3. Implémentez [les méthodes IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) appropriées pour votre fournisseur. Selon votre fournisseur, vous n’avez pas besoin d’implémenter les quatre méthodes dans **IMAPIStatus**. Chaque fournisseur doit implémenter une version en lecture seule des méthodes de l’interface [IMAPIProp : IUnknown](imapipropiunknown.md) et de la méthode [IMAPIStatus::ValidateState.](imapistatus-validatestate.md) 

   Les fournisseurs de transport doivent également implémenter [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)et tous les fournisseurs doivent prendre en charge [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md). Toutefois, la prise [en charge d’IMAPIStatus::ChangePassword est](imapistatus-changepassword.md) facultative. Seuls les fournisseurs de services qui nécessitent des mots de passe et qui souhaitent autoriser les utilisateurs à les modifier par programme doivent implémenter cette méthode. Pour chaque méthode prise en charge, définissez le bit correspondant dans **PR_RESOURCE_METHODS** propriété. Par exemple, si vous ne prenons **en charge que ValidateState** et **SettingsDialog,** **PR_RESOURCE_METHODS** les paramètres suivants : 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   Les clients doivent vérifier la valeur de **PR_RESOURCE_METHODS** avant d’appeler votre objet d’état. Gérer les appels à l’une de vos méthodes non pris en charge en renvoyant MAPI_E_NO_SUPPORT. 
    
4. Appelez [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) pendant l’logo pour ajouter vos lignes au tableau d’état. Passez un tableau de valeurs de propriété qui contient les informations de colonne pour la ligne et 0 pour le _paramètre ulFlags._ Si, à un moment donné plus tard dans la session, l’état de votre fournisseur change et qu’il devient nécessaire de mettre à jour les informations de colonne, appelez à nouveau **ModifyStatusRow** avec l’indicateur STATUSROW_UPDATE définie. 
    
Pour plus d’informations sur les objets d’état, voir [MAPI Status Objects](mapi-status-objects.md).
  
## <a name="see-also"></a>Voir aussi

- [Fournisseurs de services MAPI](mapi-service-providers.md)

