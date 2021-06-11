---
title: Ajouter un handler d’événements
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- versionupgrade event [infopath 2007],handling events [InfoPath 2007],Changing event [InfoPath 2007],InfoPath 2007, adding event handlers,Changed event [InfoPath 2007],ContextChanged event [InfoPath 2007],Click event [InfoPath 2007],events [InfoPath 2007], adding event handlers,Sign event [InfoPath 2007],ViewSwitched event [InfoPath 2007],event handling [InfoPath 2007],Merge event [InfoPath 2007],Validating event [InfoPath 2007],Submit event [InfoPath 2007],Save event [InfoPath 2007],Loading event [InfoPath 2007]
localization_priority: Normal
ms.assetid: d69393fb-fb5a-4edb-abc0-38f5d7e80bcc
description: Cette rubrique décrit les procédures permettant d'ajouter des gestionnaires d'événements à un modèle de formulaire Microsoft InfoPath avec code managé avec Visual Studio 2012. Pour ajouter un handler d’événements à un modèle de formulaire, commencez par ouvrir le modèle de formulaire dans le Concepteur InfoPath, puis sélectionnez la commande d’interface utilisateur appropriée pour l’événement pour qui vous souhaitez écrire du code. Après avoir sélectionné la commande pour un événement dans le Concepteur InfoPath, le squelette de handler d’événements de cet événement est automatiquement sélectionné dans l’éditeur de code Visual Studio 2012.
ms.openlocfilehash: c6406ec1604355c59f4ee4818fdaea5d70f696bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427184"
---
# <a name="add-an-event-handler"></a>Ajouter un handler d’événements

Cette rubrique décrit les procédures permettant d'ajouter des gestionnaires d'événements à un modèle de formulaire Microsoft InfoPath avec code managé avec Visual Studio 2012. Pour ajouter un handler d’événements à un modèle de formulaire, commencez par ouvrir le modèle de formulaire dans le Concepteur InfoPath, puis sélectionnez la commande d’interface utilisateur appropriée pour l’événement pour qui vous souhaitez écrire du code. Après avoir sélectionné la commande pour un événement dans le Concepteur InfoPath, le squelette de handler d’événements de cet événement est automatiquement sélectionné dans l’éditeur de code Visual Studio 2012.
  
> [!IMPORTANT]
> Vous devez toujours utiliser l’interface utilisateur d’InfoPath Designer pour ajouter un handler d’événements. L’ajout d’un handler d’événements avec l’interface utilisateur génère du code de liaison d’événements dans la méthode **InternalStartup** du fichier FormCode.cs ou FormCode.vb dans votre projet de modèle de formulaire. Vous ne devez pas créer la **méthode InternalStartup** ni y ajouter de code supplémentaire vous-même. 
  
### <a name="add-an-event-handler-for-the-click-event-of-a-button-control"></a>Ajout d'un gestionnaire d'événement pour l'événement Click d'un contrôle Bouton

1. Ouvrez le modèle de formulaire dans le Concepteur InfoPath, puis ajoutez un contrôle **Bouton** au formulaire. 
    
2. Cliquez sur le bouton, puis sous l'onglet **Propriétés** du ruban, cliquez sur **Code personnalisé**.
    
    Le squelette de gestionnaire d'événements de l'événement [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) est activé dans l'éditeur de code Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-changing-validating-or-changed-event-of-a-field-or-group"></a>Ajout d'un gestionnaire d'événements pour l'événement Changing, Validating ou Changed d'un champ ou d'un groupe

1. Ouvrez le modèle de formulaire dans le Concepteur InfoPath.
    
2. Cliquez avec le bouton droit de la souris sur un contrôle d'entrée de données lié au champ ou au groupe, par exemple un contrôle **Zone de texte**. 
    
3. Pointez vers **Programmation**, puis cliquez sur l'événement pour lequel vous souhaitez créer un gestionnaire d'événements. Le squelette de gestionnaire d'événements de l'événement [Changing](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) , [Validating](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) ou [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) dans l'éditeur de code Visual Studio 2012. 
    
    > [!NOTE]
    > [!REMARQUE] La commande servant à créer un gestionnaire d'événements pour l'événement **Changing** n'est pas disponible si le paramètre de compatibilité pour le modèle de formulaire st défini sur **Formulaire de navigateur Web**. L'événement **Changing** n'est pas pris en charge dans la logique métier des modèles de formulaires publiés dans les bibliothèques de documents dans Microsoft SharePoint Server 2010 avec InfoPath Forms Services. Pour créer un gestionnaire d'événements pour l'événement **Changing**, vous devez modifier le paramètre de compatibilité sur **Éditeur InfoPath** du Concepteur InfoPath. Pour cela, cliquez sur l'onglet **Fichier**, cliquez sur **Options de formulaire**, sur **Compatibilité**, puis définissez **Type de formulaire** sur **Formulaire de l'Éditeur InfoPath**. 
  
### <a name="add-an-event-handler-for-the-loading-viewswitched-contextchanged-and-sign-events-of-a-form"></a>Ajout d'un gestionnaire d'événements pour les événements Loading, ViewSwitched, ContextChanged et Sign d'un formulaire

1. Ouvrez le modèle de formulaire dans le Concepteur InfoPath.
    
2. Sous l'onglet **Développeur** du ruban, cliquez sur l'événement de formulaire pour lequel vous souhaitez écrire un gestionnaire d'événements. 
    
    Le squelette du gestionnaire d'événements de l'événement [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) , [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) ou [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) est activé dans l'éditeur de code Visual Studio 2012. 
    
    > [!NOTE]
    > [!REMARQUE] Les commandes servant à créer un gestionnaire d'événements pour l'événement [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) ou [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) ne sont pas disponibles pour le paramètre de compatibilité du modèle de formulaire est défini sur **Formulaire de navigateur Web**. Ces événements ne sont pas pris en charge dans la logique métier des modèles de formulaires publiés dans les bibliothèques de documents Microsoft SharePoint Server 2010 avec InfoPath Forms Services. Pour créer un handler d’événements pour l’événement [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) ou [Sign,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) vous devez modifier le paramètre de compatibilité en Formulaire d’éditeur **InfoPath** dans le Concepteur InfoPath. Pour cela, cliquez sur l'onglet **Fichier**, cliquez sur **Options de formulaire**, sur **Compatibilité**, puis définissez **Type de formulaire** sur **Formulaire de l'Éditeur InfoPath**. 
  
### <a name="add-an-event-handler-for-the-submit-event-of-a-form"></a>Ajout d'un gestionnaire d'événements pour l'événement Submit d'un formulaire

1. Ouvrez le modèle de formulaire dans le Concepteur InfoPath.
    
2. Click the **File** tab, click **Submit To** on the **Info** tab, and then click ** Submit Options **.
    
3. Activez la case à cocher **Autoriser les utilisateurs à envoyer ce formulaire**, cliquez sur **Effectuer une action personnalisée à l'aide du code**, puis sur **Modifier le code**.
    
    Le squelette de gestionnaire d'événements de l'événement [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) est activé dans l'éditeur de code Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-save-event-of-a-form"></a>Ajout d'un gestionnaire d'événements pour l'événement Save d'un formulaire

1. Ouvrez le modèle de formulaire dans le Concepteur InfoPath.
    
2. Cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire** sous l'onglet **Infos**. 
    
3. Cliquez sur la catégorie **Enregistrer**, activez la case à cocher **Enregistrer au moyen d'un code personnalisé**, puis cliquez sur **Modifier**.
    
    Le squelette de gestionnaire d'événements de l'événement [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) est activé dans l'éditeur de code Visual Studio 2012. 
    
    > [!NOTE]
    > [!REMARQUE] La case à cocher **Enregistrer au moyen d'un code personnalisé** n'est pas disponible si le paramètre de compatibilité du modèle de formulaire est défini sur **InfoPath Forms Services**. L'événement [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) n'est pas pris en charge dans la logique métier des modèles de formulaires publiés dans les bibliothèques de documents dans Microsoft SharePoint Server 2010 avec InfoPath Forms Services. Pour créer un handler d’événements pour l’événement [Save,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) vous devez modifier le paramètre de compatibilité en Formulaire d’éditeur **InfoPath** dans le Concepteur InfoPath. Pour cela, cliquez sur l'onglet **Fichier**, cliquez sur **Options de formulaire**, cliquez sur **Compatibilité**, puis définissez **Type de formulaire** sur **Formulaire de l'Éditeur InfoPath**. 
  
### <a name="add-an-event-handler-for-the-versionupgrade-event-of-a-form"></a>Ajout d'un gestionnaire d'événements pour l'événement VersionUpgrade d'un formulaire

1. Ouvrez le modèle de formulaire dans le Concepteur InfoPath.
    
2. Cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire** sous l'onglet **Infos**. 
    
3. Cliquez sur la catégorie **Contrôle de version**, sélectionnez **Utiliser un événement personnalisé** dans la liste déroulante **Mettre à jour les formulaires existants**, puis cliquez sur **Modifier**.
    
    Le squelette de gestionnaire d'événements de l'événement [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) est activé dans l'éditeur de code Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-merge-event-of-a-form"></a>Ajout d'un gestionnaire d'événements pour l'événement Merge d'un formulaire

1. Ouvrez le modèle de formulaire dans le Concepteur InfoPath.
    
2. Cliquez sur l'onglet **Fichier**, puis cliquez sur **Options de formulaire** sous l'onglet **Infos**. 
    
3. Cliquez sur la catégorie **Avancé**, activez la case à cocher **Activer la fusion de formulaires**, activez la case à cocher **Fusionner à l'aide d'un code personnalisé** cliquez sur **Modifier**.
    
    Le squelette de gestionnaire d'événements de l'événement [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) est activé dans l'éditeur de code Visual Studio 2012. 
    
    > [!NOTE]
    > [!REMARQUE] La case à cocher **Fusionner à l'aide d'un code personnalisé** n'est pas disponible si le paramètre de compatibilité du modèle de formulaire est défini sur **InfoPath Forms Services**. L'événement [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) n'est pas pris en charge dans la logique métier des modèles de formulaires publiés dans les bibliothèques de documents dans Microsoft SharePoint Server 2010 avec InfoPath Forms Services. Pour créer un handler d’événements pour l’événement [Merge,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) vous devez modifier le paramètre de compatibilité en Formulaire d’éditeur **InfoPath** dans le Concepteur InfoPath. Pour cela, cliquez sur l'onglet **Fichier**, cliquez sur **Options de formulaire**, cliquez sur **Compatibilité**, puis définissez **Type de formulaire** sur **Formulaire de l'Éditeur InfoPath**. 
  
## <a name="see-also"></a>Voir aussi



[Procédure : Création d’un modèle de formulaire de base avec code](walkthrough-creating-a-basic-form-template-with-code.md)

