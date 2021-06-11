---
title: À propos de la résolution de conflit pour les types d’éléments personnalisés
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 3f0853fc-f9f2-4314-ac55-47fe1e52d019
description: Cette rubrique décrit comment résoudre les conflits pour les types d’éléments personnalisés que vous créez dans Outlook.
ms.openlocfilehash: 357dd9182f26c4e9e1e264afdee296859e7b3483
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316946"
---
# <a name="about-conflict-resolution-for-custom-item-types"></a>À propos de la résolution de conflit pour les types d’éléments personnalisés

Cette rubrique décrit comment résoudre les conflits pour les types d’éléments personnalisés que vous créez dans Outlook.
  
## <a name="conflict-resolution-for-standard-outlook-item-types"></a>Résolution des conflits pour les types d’Outlook standard

Dans Outlook, des conflits se produisent lorsque deux ou plusieurs copies du même élément ont été modifiées indépendamment les unes des autres. Outlook détecte les conflits lors de la synchronisation. Par exemple, vous pouvez mettre à jour un élément de réunion en ligne dans Outlook Web App, puis mettre à jour le même élément de réunion dans Outlook lorsque vous travaillez hors connexion. Lorsque Outlook est de nouveau en ligne et synchronise les données entre l’ordinateur client et le serveur, il détecte qu’il existe deux copies différentes du même élément de réunion.
  
Lorsque Outlook synchronise les éléments qui appartiennent à un type d’élément Outlook standard, il prend en compte les propriétés spécifiques à ce type d’élément pour détecter les conflits possibles. Outlook tente de résoudre les conflits et stocke la copie résultante dans le dossier approprié sans demander l’intervention de l’utilisateur. Dans les cas où Outlook considère qu’il est possible que la copie résultante ne contienne pas toutes les données essentielles, Outlook stocke les copies en conflit dans le dossier Conflits, sous le dossier Problèmes de synchronisation. 
  
> [!NOTE]
> Les problèmes de synchronisation et ses sous-dossiers sont masqués jusqu’à ce que vous cliquiez sur **Liste** des dossiers dans le volet de navigation. 
  
Dans ce cas, les utilisateurs peuvent choisir d’aller dans le dossier Conflits pour vérifier quels éléments étaient en conflit et s’il faut utiliser une copie dans le dossier Conflits pour remplacer la copie que Outlook a décidé de conserver.
  
## <a name="conflict-resolution-for-custom-item-types"></a>Résolution des conflits pour les types d’éléments personnalisés

### <a name="item-types-and-message-classes"></a>Types d’éléments et classes de messages
  
Tous les éléments de Outlook sont associés à une classe de message. Par exemple, par défaut, un élément de courrier est associé à l’IPM de classe de **message. Remarque**. La classe de message sert principalement à identifier le formulaire qui doit être utilisé pour afficher l’élément dans Outlook. Outlook prend en charge une liste de classes de messages qui sont mappées sur les types d’éléments intégrés à Outlook. Pour plus d’informations sur les classes de message, reportez-vous à la rubrique [Types d’éléments et classes de messages](https://msdn.microsoft.com/library/15b709cc-7486-b6c7-88a3-4a4d8e0ab292%28Office.15%29.aspx). 
  
Les utilisateurs peuvent créer des types d’éléments personnalisés, affecter des classes de message personnalisées aux types d’éléments personnalisés et Outlook utiliser un formulaire personnalisé pour afficher les types d’éléments personnalisés. Par exemple, vous pouvez Outlook un formulaire de contact personnalisé pour vos contacts professionnels. Pour ce faire, vous pouvez créer un IPM de classe de message **personnalisé. Contact.Business**, créez un formulaire personnalisé pour cette classe de message et attribuez des contacts professionnels avec cette classe de message. 
  
### <a name="registering-a-conflict-resolution-scheme-for-custom-item-types"></a>Inscription d’un schéma de résolution des conflits pour les types d’éléments personnalisés
  
Lorsque vous créez un type d’élément personnalisé, autre que la classe de message personnalisée et le formulaire personnalisé, vous devez également prendre en compte la façon dont vous souhaitez que Outlook gère les conflits entre les copies d’un élément de ce type d’élément. Par défaut, Outlook utilise un schéma de résolution commun à tous les éléments, ne prend pas en compte les propriétés spécifiques à un type d’élément et présente des copies conflictuelles pour que l’utilisateur décide. En effet, les types d’éléments personnalisés peuvent définir des champs personnalisés dans le formulaire personnalisé et peuvent avoir des propriétés personnalisées et du code personnalisé. Si vous souhaitez Outlook des propriétés spécifiques à l’élément et tenter de résoudre le conflit avec une intervention minimale de l’utilisateur, vous devez le spécifier par le biais d’un paramètre dans le Windows registre. Pour ce faire, vous pouvez utiliser l’une des deux méthodes : 
  
- En appliquant un paramètre de stratégie de groupe à l’ordinateur local qui définit la clé de Registre ConflictMsgCls. L’exemple suivant spécifie la version « 14.0 » pour Outlook 2010 : 
  
   `[HKCU]\Software\Policies\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
- En modifiant directement la clé de Registre utilisateur ConflictMsgCls. L’exemple suivant spécifie la version « 14.0 » pour Outlook 2010 : 
  
   `[HKCU]\Software\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
La définition de la résolution des conflits par le biais de la stratégie de groupe est prioritaire sur la modification directe de la clé de Registre de l’utilisateur. L’emplacement de la clé dans le Registre dépend de la version de Outlook. Vous spécifiez le nom de la classe de message personnalisée en tant que valeur sous cette clé. Spécifiez le type de la valeur en tant que **DWORD** et les données de la valeur comme l’une des valeurs indiquées dans le tableau suivant, en fonction du schéma de résolution que vous choisissez. 
  
|Data  | Description  |
|:-----|:-----|
|0  <br/> |Résolution d’éléments courante nécessitant une décision de l’utilisateur, tel qu’Outlook 2002 et versions antérieures.  <br/> |
|1  <br/> |Résolution d’élément courante qui nécessite une intervention minimale de l’utilisateur, comme utilisé Outlook depuis Outlook 2003.  <br/> |
|2  <br/> |Résolution spécifique aux éléments de courrier.  <br/> |
|3  <br/> |Résolution spécifique aux éléments de réunion.  <br/> |
|4   <br/> |Résolution spécifique aux éléments de rendez-vous.  <br/> |
|5   <br/> |Résolution spécifique aux éléments de contact.  <br/> |
|6   <br/> |Résolution spécifique aux éléments de tâche.  <br/> |
|7   <br/> |Résolution spécifique aux éléments de note resserrante.  <br/> |
|8   <br/> |Résolution spécifique aux éléments de journal.  <br/> |
   
Si vous spécifiez l’un des schémas de résolution spécifiques à l’élément (données clés 2 à 8),  Outlook essaiera de résoudre automatiquement les conflits dans les champs spécifiques à l’élément (par **exemple,** les champs Début et Fin d’un élément de rendez-vous) sans intervention de l’utilisateur. Si Outlook considère que la résolution peut entraîner la perte de données essentielles, Outlook conserve les copies conflictuelles dans le dossier Conflits et les utilisateurs peuvent choisir d’aller dans le dossier Conflits pour résoudre manuellement ces éléments et remplacer la résolution automatique. 
  
En utilisant le même exemple de contacts professionnels ci-dessus, si vous souhaitez spécifier le schéma de résolution spécifique à l’élément de contact pour la classe de message **personnalisée IPM. Contact.Business**, vous pouvez l’ajouter en tant que **valeur DWORD** sous  `[HKCU]\Software\Microsoft\Office\15.0\Outlook\Options\ConflictMsgCls` et spécifier 5 comme données. 
  
> [!NOTE]
> Outlook utilise toujours un schéma de résolution spécifique aux éléments de rendez-vous pour les classes de message personnalisées basées sur la classe de message de **rendez-vous, IPM. Rendez-vous** (par exemple, **IPM. Appointment.Personal**). 
  
## <a name="see-also"></a>Voir aussi

- [Éléments Outlook](https://msdn.microsoft.com/library/6ea4babf-facf-4018-ef5a-4a484e55153a%28Office.15%29.aspx)

