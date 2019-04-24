---
title: Implémentation d’un objet d’état
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 48fd3e28-c2d2-474d-9487-5e2f08ca7319
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: e97efb70716ffbd7fa98f980ce8520cfcb988532
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336336"
---
# <a name="status-object-implementation"></a>Implémentation d’un objet d’état

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tous les fournisseurs de services doivent implémenter un objet Status et fournir les propriétés de celui-ci à la table d'état de session. Vous pouvez inclure une ou plusieurs lignes dans le tableau d'État, en fonction du nombre de ressources que vous contrôlez. Un fournisseur de transport, par exemple, doit créer une ligne dans la table d'État pour chaque file d'attente de messages qu'il gère. Lorsque des modifications se produisent, la ligne de table d'État appropriée doit être mise à jour. Les objets d'État sont implémentés pour fournir l'accès aux informations incluses dans la table d'État et à des informations supplémentaires non incluses dans le tableau.
  
### <a name="to-implement-a-status-object"></a>Pour implémenter un objet Status

1. Implémentez la méthode **OpenStatusEntry** de votre objet Logon. Lorsque les clients souhaitent ouvrir votre objet d'État, ils appellent [IMAPISession:: OpenEntry](imapisession-openentry.md). MAPI remplit la demande d'ouverture en appelant la méthode **OpenStatusEntry** de votre fournisseur, ce qui entraîne l'ouverture de son objet d'État par votre fournisseur et revient au client un pointeur vers son implémentation **IMAPIStatus** . Dans votre implémentation **OpenStatusEntry** , procédez comme suit: 
    
   1. Effectuez les tâches suivantes si votre objet d'ouverture de session n'a pas encore créé d'objet d'État:
    
      1. Appelez la méthode [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) de l'objet de prise en charge pour accéder à la section de profil de votre fournisseur. 
          
      2. Crée un objet d'État.
          
      3. Stockez une référence à la section de profil dans l'objet d'état de votre fournisseur et appelez la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) de la section de profil pour incrémenter son décompte de référence. 
          
      4. Stockez une référence à l'objet Logon dans l'objet Status de votre fournisseur et appelez la méthode **IUnknown:: AddRef** de l'objet Logon pour incrémenter son décompte de référence. 
          
      5. Stockez une référence à l'objet Status dans l'objet Logon de votre fournisseur.
    
   2. Appelez la méthode **IUnknown:: AddRef** de l'objet Status pour incrémenter son décompte de référence dans l'objet Logon. 
    
   3. Définissez la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) de l'objet Status sur MAPI_STATUS.
    
   4. Définissez le paramètre de sortie _lppMAPIStatus_ de sorte qu'il pointe sur l'objet d'État et qu'il soit retourné. 
    
   5. Vérifiez le paramètre d'entrée _ulFlags_ . S'il est défini sur MAPI_MODIFY et que votre fournisseur prend en charge l'accès en lecture/écriture à son objet d'État, renvoie un objet accessible en écriture. Toutefois, si votre fournisseur ne prend pas en charge l'accès en lecture/écriture à son objet d'État, n'échouez pas. Renvoyer un objet Status qui est en lecture seule. Les clients qui s'attendent à recevoir des objets d'État en lecture/écriture doivent vérifier que l'autorisation de lecture/écriture a été accordée avant d'essayer d'effectuer des modifications. 
    
2. Définissez tous les objets d'État et les propriétés de table d'État requis. Les propriétés que vous incluez dans votre ligne de table d'État doivent être disponibles via votre objet d'État, à l'exception des propriétés calculées par MAPI. Les propriétés requises sont les suivantes:
    
   - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   - **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))
    
   - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   - **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))
    
   - **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
    
   - **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))
    
   - **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))
    
3. Implémentez les méthodes [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) appropriées pour votre fournisseur. En fonction de votre fournisseur, il n'est pas nécessaire d'implémenter toutes les quatre méthodes dans **IMAPIStatus**. Chaque fournisseur doit implémenter une version en lecture seule des méthodes de l'interface [IMAPIProp: IUnknown](imapipropiunknown.md) et de la méthode [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) . 

   Les fournisseurs de transport doivent également implémenter [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md)et tous les fournisseurs doivent prendre en charge [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md). Toutefois, la prise en charge de [IMAPIStatus:: ChangePassword](imapistatus-changepassword.md) est facultative. Seuls les fournisseurs de services qui nécessitent des mots de passe et souhaitent autoriser les utilisateurs à les modifier par programmation doivent implémenter cette méthode. Pour chaque méthode que vous prenez en charge, définissez le bit correspondant dans la propriété **PR_RESOURCE_METHODS** . Par exemple, si vous prenez en charge **ValidateState** et **SettingsDialog** uniquement, définissez **PR_RESOURCE_METHODS** comme suit: 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   Les clients doivent vérifier la valeur de **PR_RESOURCE_METHODS** avant d'essayer d'appeler votre objet d'État. Gérer les appels à l'une de vos méthodes non prises en charge en retournant MAPI_E_NO_SUPPORT. 
    
4. Appelez [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) pendant l'ouverture de session pour ajouter la ou les lignes à la table d'État. TransMettez un tableau de valeurs de propriété qui contient les informations de colonne pour la ligne et 0 pour le paramètre _ulFlags_ . Si, plus loin dans la session, l'état de votre fournisseur change et qu'il devient nécessaire de mettre à jour les informations de colonne, appelez de nouveau **ModifyStatusRow** avec l'indicateur STATUSROW_UPDATE défini. 
    
Pour plus d'informations sur les objets d'État, voir [MAPI Status Objects](mapi-status-objects.md).
  
## <a name="see-also"></a>Voir aussi

- [Fournisseurs de services MAPI](mapi-service-providers.md)

