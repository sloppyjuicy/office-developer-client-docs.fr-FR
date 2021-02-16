---
title: Gérer une résolution élevée et redimensionner la résolution dans votre solution Office
description: Mettre à jour votre solution Office tels que les volets de tâches personnalisés, ou les contrôles ActiveX, pour prendre en charge des moniteurs à haute résolution.
ms.date: 03/09/2019
localization_priority: Normal
ms.openlocfilehash: 78179b958bc57137c0565b8b1ca5feb40f61fe0e
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293477"
---
# <a name="handle-high-dpi-and-dpi-scaling-in-your-office-solution"></a>Gérer une résolution élevée et redimensionner la résolution dans votre solution Office

De nombreuses configurations d’écran et d’ordinateur prennent désormais en charge une résolution élevée PPP (points par pouce) et peuvent mettre en contact plusieurs moniteurs de différentes tailles et densités exprimées en pixels. Ceci nécessite que les applications s’ajustent quand l’utilisateur déplace l’application sur un moniteur avec une résolution différente ou modifie le niveau de zoom. Les applications qui ne prennent pas en charge la mise à l’échelle PPP peuvent avoir un bon rendu sur moniteurs à faible PPP mais auront l’air étirées et floues sur un écran haute résolution. 

Les applications Office 2016, telles que Word et Excel, ont été mises à jour pour répondre aux modifications d’échelle. Toutefois, votre solution Office doit également répondre aux modifications pour dessiner correctement lorsque le PPP change. Cet article décrit comment Office prend en charge les PPP dynamiques et quelles opérations vous pouvez effectuer pour assurer la meilleure expérience d’affichage pour votre solution extensibilité Office pour gérer le redimensionnement PPP. 

## <a name="dpi-scaling-symptoms-in-your-solution"></a>Symptômes de redimensionnement PPP dans votre solution

Windows applique le redimensionnement PPP lorsqu’une application est déplacée d’un type d’affichage à un autre avec une résolution différente. Cela se produit lorsque vous faites glisser une application vers un autre écran ou utilisez l’ancrage de votre ordinateur portable. Si votre solution Office est affectée négativement par le redimensionnement PPP, vous pouvez constater un ou plusieurs des symptômes suivants :

- Les fenêtres apparaissent au mauvais emplacement ou ont une taille incorrecte.
- Les éléments tels que les boutons et étiquettes apparaissent dans un emplacement incorrect dans la fenêtre de votre solution.
- Les polices et images sont trop petites, trop volumineuses ou à un emplacement incorrect.

Les types suivants de solutions Office peuvent être affectés par la mise à l’échelle PPP :

- Compléments VSTO
- Volets des tâches personnalisés
- Compléments COM
- Contrôles ActiveX
- Extensions de ruban
- Serveurs OLE
- Compléments Office web

## <a name="windows-dpi-awareness-modes"></a>Modes de présence PPP Windows

Dans cet article, nous allons faire référence aux modes de sensibilisation PPP que Windows prend en charge. Chaque mode de présence PPP prend en charge différentes fonctionnalités, comme décrit dans le tableau suivant. Il s’agit d’une description simplifiée des modes afin d’expliquer comment les solutions Office les prennent en charge. Pour plus d’informations sur les modes de présence PPP, voir [Développement d’applications bureau haute résolution sur Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows).

|Mode  |Description  |Lorsque la résolution change  |
|---------|---------|---------|
|Système PPP ignoré |  L’application s’affiche toujours comme si elle est sur une résolution de valeur 96. |  L’application est étirée bitmap à la taille attendue sur l’affichage principal et secondaire.    |
|Système PPP pris en compte |  L’application détecte la résolution du moniteur principal connecté à Windows, mais ne peut pas répondre aux modifications PPP. Pour plus d’informations, voir la section Configurer Windows pour corriger les applications [floues](#configure-windows-to-fix-blurry-apps) dans cet article.  | L’application est étirée bitmap lorsqu’elle est déplacée vers un nouvel affichage avec une résolution différente.    |
|Par moniteur PPP pris en compte |  L’application est capable de s’afficher correctement d’elle-même lorsque le PPP change.  |   Windows envoie des notifications PPP aux fenêtres de niveau supérieur dans l’application, de sorte qu’elle peut ajuster son affichage en cas de modification de la résolution.     |
|Par moniteur v2 |  L’application est capable de s’afficher correctement d’elle-même lorsque le PPP change.  |   Windows envoie des notifications PPP aux fenêtres de niveau supérieur et aux fenêtres enfants dans l’application, de sorte qu’elle peut ajuster son affichage en cas de modification de la résolution. |

## <a name="how-office-supports-dpi-scaling"></a>Comment Office prend en charge la mise à l’échelle PPP

Le facteur le plus significatif dans la détermination de comment votre solution Office peut gérer la mise à l’échelle PPP est si votre solution est une fenêtre de niveau supérieur ou une fenêtre enfant. L’image suivante montre quelques exemples de solutions Office opérationnelles en tant que fenêtres de niveau supérieur ou enfants, et quel mode de présence PPP elles utilisent sur la mise à jour Windows avril 2018 (1803) et versions ultérieures.

![Excel hébergeant un contrôle ActiveX et un volet de tâches personnalisé en tant que fenêtre enfant. Un complément COM/VSTO distinct s’exécute comme une fenêtre de niveau supérieur. Office est une fenêtre de niveau supérieur.](./media/office-dpi-awareness-for-solution-types.png)

Dans cette image :
- La fenêtre de niveau supérieur COM/VSTO est Par moniteur PPP pris en compte.
- La fenêtre enfant de contrôle ActiveX est Système PPP pris en compte.
- La fenêtre de niveau supérieur Office est Par moniteur PPP pris en compte.
- La fenêtre enfant de volet de tâches personnalisé est Système PPP pris en compte.

## <a name="managing-thread-dpi-context"></a>La gestion de contexte de thread PPP

Lorsque l’application Office hôte démarre, son thread principal est exécuté en contexte Par moniteur PPP pris en compte. Lorsque votre code de solution crée des threads ou reçoit des appels à partir d’Office, vous devez gérer le contexte PPP du thread.

### <a name="creating-new-threads-with-the-correct-dpi-context"></a>Création de nouveaux threads avec le contexte PPP correct

Si votre solution crée des threads supplémentaires, Office obligent les threads à utiliser un contexte Par moniteur PPP pris en compte. Si votre code attend un contexte différent, vous devez utiliser la fonction [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) pour définir la présence de thread PPP prévue. 

### <a name="build-a-context-block-for-incoming-thread-calls"></a>Créer un bloc de contexte pour les appels thread entrants 

![Diagramme montrant le bloc de contexte dans l’application Office passant le thread à un contexte Système pris en compte sur les appels à votre fenêtre de niveau supérieur.](./media/thread-dpi-awareness-context-block.png)

Votre solution interagit avec son application Office hôte, donc vous aurez des appels entrants pour votre solution à partir d’Office, tels que des rappels d’événement. Lorsque Office appelle votre solution, celui-ci comporte un bloc de contexte qui force le contexte de thread en contexte Système PPP pris en compte. Vous devez modifier le contexte du thread pour qu’il soit conforme à la présence de résolution de la fenêtre. Vous pouvez implémenter un bloc de contexte similaire pour basculer le contexte du thread sur les appels entrants. Utilisez la fonction [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) pour modifier le contexte pour correspondre au contexte de votre fenêtre. 

> [!NOTE]
> Votre bloc de contexte doit restaurer le contexte du thread PPP d’origine avant d’appeler d’autres composants en dehors de votre code de solution.

#### <a name="managed-code-context-block"></a>Gérer le bloc de contexte code

L’exemple de code suivant montre comment créer votre propre bloc de contexte.

```csharp
public struct DPI_AWARENESS_CONTEXT
        {
            private IntPtr value;

            private DPI_AWARENESS_CONTEXT(IntPtr value)
            {
                this.value = value;
            }

            public static implicit operator DPI_AWARENESS_CONTEXT(IntPtr value)
            {
                return new DPI_AWARENESS_CONTEXT(value);
            }

            public static implicit operator IntPtr(DPI_AWARENESS_CONTEXT context)
            {
                return context.value;
            }

            public static bool operator ==(IntPtr context1, DPI_AWARENESS_CONTEXT context2)
            {
                return AreDpiAwarenessContextsEqual(context1, context2);
            }

            public static bool operator !=(IntPtr context1, DPI_AWARENESS_CONTEXT context2)
            {
                return !AreDpiAwarenessContextsEqual(context1, context2);
            }

            public override bool Equals(object obj)
            {
                return base.Equals(obj);
            }

            public override int GetHashCode()
            {
                return base.GetHashCode();
            }
        }

        private static DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_HANDLE = IntPtr.Zero;

        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_INVALID = IntPtr.Zero;
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_UNAWARE = new IntPtr(-1);
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_SYSTEM_AWARE = new IntPtr(-2);
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE = new IntPtr(-3);
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 = new IntPtr(-4);

        public static DPI_AWARENESS_CONTEXT[] DpiAwarenessContexts =
        {
            DPI_AWARENESS_CONTEXT_UNAWARE,
            DPI_AWARENESS_CONTEXT_SYSTEM_AWARE,
            DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE,
            DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2
        };

class DPIContextBlock : IDisposable
    {
        private DPI_AWARENESS_CONTEXT resetContext;
        private bool disposed = false;

        public DPIContextBlock(DPI_AWARENESS_CONTEXT contextSwitchTo)
        {
            resetContext = SetThreadDpiAwarenessContext(contextSwitchTo);
         }

        public void Dispose()
        {
            Dispose(true);
            GC.SuppressFinalize(this);
        }

        protected virtual void Dispose(bool disposing)
        {
            if (!disposed)
            {
                if (disposing)
                {
                    SetThreadDpiAwarenessContext(resetContext);
                }
            }
            disposed = true;
        }
    }
```

#### <a name="native-code-context-block"></a>Bloc de contexte code natif

```cpp
#include <winuser.h>
/* DpiAwarenessContextBlock can be used to simplify setting and resetting the DPI_AWARENESS_CONTEXT of
the current thread.  When the object is constructed, the DPI_AWARENESS_CONTEXT is set, and when the object is
destructed, the DPI awareness context is reverted to the previous awareness context at construct time.

This object allows us to write code such as:

// Thread state is currently DPI_AWARENESS_SYSTEM_AWARE
if (condition)
{
DpiAwarenessContextBlock perMonitorAware(DPI_AWARENESS_PER_MONITOR_AWARE);
... // Create a top-level hwnd with the current thread state, DPI_AWARENESS_PER_MONITOR_AWARE
}
// Thread state automatically returns to DPI_AWARENESS_SYSTEM_AWARE

*/
class DpiAwarenessContextBlock
{
public:
      DpiAwarenessContextBlock(DPI_AWARENESS_CONTEXT dpiContext) noexcept;
      ~DpiAwarenessContextBlock();

      // Copy and move are not to be used with these context objects
      DpiAwarenessContextBlock(const DpiAwarenessContextBlock&) = delete;
      DpiAwarenessContextBlock(DpiAwarenessContextBlock&&) = delete;

private:
      DPI_AWARENESS_CONTEXT m_contextReversalType;
      bool m_doContextSwitch;
};

inline DpiAwarenessContextBlock::DpiAwarenessContextBlock(DPI_AWARENESS_CONTEXT dpiContext) noexcept
{
      m_contextReversalType = SetThreadDpiAwarenessContext(dpiContext);
}

inline DpiAwarenessContextBlock::~DpiAwarenessContextBlock()
{
      SetThreadDpiAwarenessContext(m_contextReversalType);
}
```

<h2 id="top-level-window-management">Gestion de fenêtre de niveau supérieur</h2>

Lors du démarrage des applications Office, un appel est effectué à [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) comme DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE. Dans ce contexte, les modifications PPP sont envoyées à HWND de n’importe quelle fenêtre de niveau supérieur dans le processus en cours d’exécution avec moniteur PPP pris en compte. Les fenêtres de niveau supérieur sont les fenêtres d’application Office, et toute autre fenêtre de niveau supérieur créée par votre solution. Lorsqu’une application Office est déplacée vers un nouvel affichage, elle reçoit une notification afin qu’elle puisse se mettre à l’échelle dynamiquement et s’afficher correctement dans la résolution du nouvel affichage. Votre solution Office pouvez créer des fenêtres de niveau supérieur qui se trouvent dans n’importe quel mode de présence PPP. Vos fenêtres de niveau supérieur peuvent également répondre aux modifications PPP en écoutant les messages Windows pour les modifications.

Si vous créez des fenêtres enfants apparentées à votre fenêtre de niveau supérieur, vous pouvez également les définir sur n’importe quel mode de présence PPP. Toutefois, si vous utilisez le mode Par moniteur PPP pris en compte, vos fenêtres enfant ne recevront pas les notifications de modification PPP.  Pour plus d’informations sur les modes de présence PPP Windows, voir [Développement d’applications bureau haute résolution sur Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows).

## <a name="child-window-management"></a>Gestion de fenêtre enfant

Lorsque vous travaillez avec des contrôles ActiveX et volets de tâches personnalisés, Office crée la fenêtre enfant pour votre solution. Vous pouvez créer des fenêtres enfants supplémentaires, mais vous devez tenir compte de la présence PPP de la fenêtre parent. Office est exécuté en mode de présence Per moniteur PPP, ce qui signifie qu’aucune fenêtre enfant dans votre solution ne recevra pas de notifications de modification PPP. Uniquement le mode Par moniteur v2 prend en charge l’envoi de modifications PPP aux fenêtres enfant (Office ne prend pas en charge Par moniteur v2). Toutefois, pour les contrôles ActiveX, il existe une solution de contournement. Pour plus d’informations, voir la section [Contrôles ActiveX](#activex-controls) plus loin dans cette rubrique.

> [!NOTE]
> Si votre fenêtre enfant crée une fenêtre de niveau supérieur, vous pouvez utiliser n’importe quel mode de présence PPP pour la nouvelle fenêtre de niveau supérieur. Pour plus d’informations sur la gestion des fenêtres de niveau supérieur, voir la section [Gestion de la fenêtre de niveau supérieur](#top-level-window-management) de cet article.

Vous verrez deux différents modes PPP appliqués à la fenêtre enfant, selon la version d’Office Windows 10 en cours d’exécution.

### <a name="office-dpi-behavior-on-windows-fall-creators-update-1709"></a>Comportement Office PPP sur Windows Fall Creators Update (1709)

Étant donné que les applications Office utilisent le mode de présence par moniteur, les fenêtres enfants de votre solution seront également créées en mode de présence Per moniteur PPP. Cela signifie que Windows attend de votre solution qu’elle se mette à jour lorsqu’elle s’affiche dans un nouveau PPP.  Étant donné que la fenêtre ne peut pas recevoir de notifications de modification PPP, l’interface utilisateur de votre solution peut être incorrecte. 

![Diagramme montrant les fenêtres enfants en cours d’exécution dans un contexte Par moniteur PPP pris en compte sur Windows Fall Creators Update (1709).](./media/office-dpi-behavior-on-windows-fall-creators-update.png)

### <a name="office-dpi-behavior-on-windows-april-2018-update-1803"></a>Comportement Office PPP sur Mise à jour Windows avril 2018 (1803)

Avec la mise à jour Windows avril 2018 (1803) et versions ultérieures, le comportement d’hébergement Office PPP utilise la mise à l’échelle PPP en mode mixte pour certains scénarios. Cela permet aux fenêtres de système PPP pris en compte d’être liées aux fenêtres Office configurées sur Par moniteur PPP pris en compte. Cela permet de garantir une meilleure compatibilité lorsque la résolution change lorsque les fenêtres sont étirées bitmap. Les fenêtres peuvent toujours être floues en raison de l’étirement bitmap.

![Diagramme montrant les fenêtres enfants en cours d’exécution dans un contexte Par système PPP pris en compte sur Windows mise à jour avril 2018 (1803).](./media/office-dpi-behavior-on-windows-april-2018-update.png)

Lorsque vous créez nouveau fenêtre enfant, assurez-vous qu’elles correspondent à la résolution de présence de leur fenêtre parent. Vous pouvez utiliser la [fonction GetWindowDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext) pour obtenir la connaissance DEPI de la fenêtre parente. Pour plus d’informations sur la cohérence de présence PPP, voir la section « Réinitialisation forcée de présence à l’échelle de processus PPP » dans [Développement d’applications bureau pour haute résolution sur Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics).

> [!NOTE]
> Vous ne pouvez pas dépendre de la présence de processus PPP car cela peut renvoyer [PROCESS_SYSTEM_DPI_AWARE](https://docs.microsoft.com/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness) même lorsque le contexte de présence du thread principal PPP de l’application est [DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE](https://docs.microsoft.com/windows/desktop/hidpi/dpi-awareness-context). Utilisez la fonction [GetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext) pour obtenir le contexte de présence du thread PPP.

## <a name="office-and-windows-dpi-compatibility-settings"></a>Paramètres de compatibilité Office et Windows PPP

Lorsque les utilisateurs rencontrent des compléments ou des solutions qui ne sont pas affichés correctement, certains paramètres de compatibilité peuvent vous aider à corriger le problème.

<h3 id="office-compatibility">Configurer Office pour optimiser la compatibilité</h3>

Office a défini un paramètre pour optimiser la compatibilité lors de la transition vers différentes échelles PPP sur différents écrans. Le mode de compatibilité désactive la mise à l’échelle PPP afin que tout le contenu dans Office soit étiré bitmap lors du déplacement vers un affichage utilisant une échelle PPP différente. 

Le mode de compatibilité force Office à s’exécuter en mode système PPP pris en compte. Cela amène les fenêtres d’application à un étirement bitmap et peut avoir un aspect flou comme effet secondaire. Votre solution Office ne peut pas contrôler ce paramètre, car l’utilisateur choisit celui-ci. Utiliser le mode de compatibilité d’affichage permet de résoudre la plupart des problèmes d’apparence. Pour plus d’informations, voir [Support Office pour l’affichage haute définition](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d). 

### <a name="configure-windows-to-fix-blurry-apps"></a>Configurez Windows pour résoudre les application floues

Windows 10 (Version 1803) et versions suivantes ont défini un paramètre pour corriger les applications afin qu’elles ne soient pas floues. Il s’agit d’un autre paramètre à essayer si votre solution n’est pas affichée correctement. Votre solution Office ne peut pas contrôler ce paramètre, car l’utilisateur choisit celui-ci. Pour plus d’informations, voir [Corriger les applications qui s’affichent floues dans Windows 10](https://support.microsoft.com/en-us/help/4091364/windows-10-fix-blurry-apps).

## <a name="how-to-support-dpi-scaling-in-your-solution"></a>Comment prendre en charge le redimensionnement PPP dans votre solution

Certaines solutions peuvent recevoir et répondre aux modifications PPP. Certaines ont une solution de contournement si elles ne peuvent pas recevoir des notifications. Le tableau suivant répertorie les détails pour chaque type de solution.

<table>
    <thead>
        <tr>
            <th>Type de solution</th>
            <th>Type de fenêtre</th>
            <th>Peut répondre au redimensionnement PPP</th>
            <th>Plus de détails</th>
        </tr>
    </thead>
<tbody>
    <tr>
        <td rowspan="2"><a href="#vsto-add-ins">Complément VSTO</a></td>
        <td>Niveau supérieur et descendants</td>
        <td>Oui</td>
        <td>Voir <a href="#vsto-add-ins">Conseils complément VSTO</a>.</td>
    </tr>
<tr>
        <td>Enfant apparenté à la fenêtre Office</td>
        <td>Non</td>
        <td>Voir <a href="#office-compatibility">Configurer Office pour optimiser la compatibilité</a>.</td>
</tr>
    <tr>
        <td rowspan="2"><a href="#custom-task-panes">Volet Office personnalisé</a></td>
        <td>Niveau supérieur et descendants</td>
        <td>Oui</td>
        <td>Voir <a href="#top-level-window-management">Conseils fenêtre de niveau supérieur</a>.</td>
    </tr>
<tr>
        <td>Enfant apparenté à la fenêtre Office</td>
        <td>Non</td>
        <td>Voir <a href="#office-compatibility">Configurer Office pour optimiser la compatibilité</a>.</td>
</tr>
    <tr>
        <td rowspan="2"><a href="#com-add-ins">Complément COM</a></td>
        <td>Niveau supérieur et descendants</td>
        <td>Oui</td>
        <td>Voir <a href="#com-add-ins">Conseils complément COM</a>.</td>
    </tr>
<tr>
        <td>Enfant apparenté à la fenêtre Office</td>
        <td>Non</td>
        <td>Voir <a href="#office-compatibility">Configurer Office pour optimiser la compatibilité</a>.</td>
</tr>
    <tr>
        <td rowspan="2"><a href="#activex-controls">Contrôle ActiveX</a></td>
        <td>Niveau supérieur et descendants</td>
        <td>Oui</td>
        <td>Voir <a href="#activex-controls">Conseils contrôle ActiveX</a>.</td>
    </tr>
    <tr>
        <td>Enfant apparenté à la fenêtre Office</td>
        <td>Oui</td>
    </tr>
    <tr>
        <td><a href="#web-add-ins">Complément Web</a></td>
        <td>N/A</td>
        <td>Oui</td>
        <td>Voir <a href="#web-add-ins">Conseils complément Office web</a>.</td>
    </tr>
    <tr>
        <td><a href="#ribbon-extensibility">Extension du ruban</a></td>
        <td>N/A</td>
        <td>N/A</td>
        <td>Voir <a href="#ribbon-extensibility">Conseils extension ruban</a>.</td>
    </tr>
    <tr>
        <td><a href="#ole">Client ou serveur OLE</a></td>
        <td>N/A</td>
        <td>N/A</td>
        <td>Voir <a href="#ole">Conseils client/serveur OLE</a>.</td>
    </tr>
</tbody>
</table>

<h3 id="vsto-add-ins">Complément VSTO</h3>

Si votre complément VSTO crée des fenêtres enfant apparentées à n’importe quelle fenêtre Office, assurez-vous qu’elles correspondent à la résolution de présence de leur fenêtre parent. Vous pouvez utiliser la fonction[GetWindowdpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext) pour obtenir la résolution de présence de la fenêtre parent. Vos fenêtres enfants ne recevront pas les notifications de modification PPP. Si votre solution n’est pas affichée correctement, les utilisateurs doivent configurer Office en mode de compatibilité.

Pour n’importe quelle fenêtre de niveau supérieur que votre complément VSTO crée, vous pouvez les définir sur n’importe quel mode de présence PPP. L’exemple de code suivant explique comment configurer la présence de PPP souhaitée et comment répondre aux modifications PPP. Vous devrez également ajuster votre app.config, comme décrit dans l’article [Prise en charge de la haute résolution dans Windows Forms](https://docs.microsoft.com/dotnet/framework/winforms/high-dpi-support-in-windows-forms). 

```csharp
using System;
using System.Diagnostics;
using System.Drawing;
using System.Runtime.InteropServices;
using System.Windows.Forms;

namespace SharedModule
{
    // DpiAwareWindowsForm
    // For any top level winform you create, derive from the DpiWindowsForm class
    // if you are creating Windows Forms with the Dpi Awareness Context set to 
    // DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE or DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2
    //
    // For example, if you Window form class is defined as:
    //    public partial class TopLevelWinForm : Form
    //
    // update to:
    //    public partial class TopLevelWinForm : DpiAwareWindowsForm
    //
    // When showing the form, call SetThreadDpiAwarenessContext() or use a context block to
    // to set the desired Dpi Awareness Context.
    //
    // For example, here is code to show a Windows Form using a context block as Per Monitor Aware v2.
    //
    //    DPIContextBlock context = new DPIContextBlock(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2);
    //    TopLevelWinForm frm = new TopLevelWinForm();
    //    frm.Show();
    //
    public partial class DpiAwareWindowsForm : Form
    {
        private SizeF m_newDpi = SizeF.Empty;
        private SizeF m_oldDpi = SizeF.Empty;

        public DpiAwareWindowsForm()
        {
            this.HandleCreated += new EventHandler((sender, args) =>
            {
                m_oldDpi = m_newDpi = DPIHelper.GetDpiForWindowSizeF(this.Handle);
            });
        }

        public void OnDpiChangedEvent(RECT newRect)
        {
            this.SuspendLayout();

            // Resize form
            this.Width = newRect.Width;
            this.Height = newRect.Height;

            // Resize controls and set font sizes
            ScaleAllChildControls(this.Controls, m_oldDpi.Width, m_newDpi.Width);
            this.ResumeLayout(true);
        }

        // Additional changes may be needed for controls that set Anchor or Dock properties 
        private void ScaleAllChildControls(Control.ControlCollection controls, float oldDpi, float newDpi)
        {
            float scaleFactorChange = newDpi / oldDpi;

            foreach (Control control in controls)
            {
                control.Top = (int)(control.Top * scaleFactorChange);
                control.Left = (int)(control.Left * scaleFactorChange);
                control.Width = (int)(control.Width * scaleFactorChange);
                control.Height = (int)(control.Height * scaleFactorChange);
                control.Font = ScaleFont(control.Font, oldDpi, newDpi);
            }
        }

        private Font ScaleFont(Font font, float oldDpi, float newDpi)
        {
            float fontSizePx = 0.0f;
            float fontSizePt = 0.0f;

            fontSizePx = font.SizeInPoints / 72 * oldDpi;
            fontSizePt = fontSizePx * (newDpi / oldDpi) * 72 / oldDpi;

            return new Font(font.Name, fontSizePt, font.Style, GraphicsUnit.Point);
        }

        protected override void WndProc(ref Message m)
        {
            switch ((DPIHelper.WinMessages)m.Msg)
            {
                case DPIHelper.WinMessages.WM_DPICHANGED:
                    // Marshal the value in the lParam into a Rect.
                    RECT newDisplayRect = (RECT)Marshal.PtrToStructure(m.LParam, typeof(RECT));

                    // Remember current DPI and calculate current from WParam.
                    // Both X and Y are the same on Windows for Dpi.
                    m_oldDpi = m_newDpi;

                    m_newDpi.Width = (float)(m.WParam.ToInt32() >> 16);
                    m_newDpi.Height = (float)(m.WParam.ToInt32() & 0x0000FFFF);

                    // DPI should be the same for both width and height on Windows devices.
                    Debug.Assert(m_newDpi.Height == m_newDpi.Width);

                    if (m_oldDpi.Width != m_newDpi.Width)
                    {
                        OnDpiChangedEvent(newDisplayRect);
                    }
                    base.DefWndProc(ref m);
                    break;
                default:
                    base.WndProc(ref m);
                    break;
            }
        }
    }
}
```

<h3 id="custom-task-panes">Volets des tâches personnalisés</h3>

Un volet de tâches personnalisé est créé comme fenêtre enfant par Office. Lors de l’exécution sur Windows Fall Creators Update (1709), votre volet Office personnalisé s’exécute en utilisant le même mode de présence PPP qu’Office. Lors de l’exécution sur la mise à jour avril 2018 Windows (1803) et versions ultérieures, votre volet de tâches personnalisé s’exécutera sur le mode de présence système PPP. 

Comme les volets de tâches personnalisés sont des fenêtres enfants, ils ne peuvent pas recevoir de notifications PPP. S’ils sont affichés incorrectement, l’utilisateur devra utiliser le[mode de compatibilité Office PPP](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).
Si votre volet de tâches personnalisé crée des fenêtres de niveau supérieur, ces fenêtres peuvent s’exécuter dans n’importe quel mode de présence PPP et recevoir des notifications de modification PPP. Pour plus d’informations, voir la section [Gestion de la fenêtre de niveau supérieur](#top-level-window-management) de cet article.

<h3 id="com-add-ins">Compléments COM</h3>

Les compléments COM qui créent des fenêtres de niveau supérieur peuvent recevoir des notifications PPP. Vous devez créer un [bloc de contexte](#build-a-context-block-for-incoming-thread-calls) pour définir le thread à la présence PPP souhaitée pour la fenêtre, puis créer la fenêtre. Il y a beaucoup à gagner à gérer les notifications PPP correctement, veillez donc à lire [Développement d’applications bureau à haute résolution sur Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics) pour plus d’informations.

Le message [WM_DPICHANGED](https://docs.microsoft.com/windows/desktop/hidpi/wm-dpichanged) est envoyé lorsque le PPP pour une fenêtre a changé.  Dans le code non géré, ce message est géré par la [Procédure de fenêtre](https://docs.microsoft.com/windows/desktop/winmsg/using-window-procedures) pour le HWND.  Un exemple de code de modification du gestionnaire PPP est accessible dans l’article WM_DPICHANGED. 

Les compléments COM qui montrent les fenêtres enfants apparentées à une fenêtre dans Office ne peuvent pas recevoir de notifications PPP. S’ils sont affichés incorrectement, l’utilisateur devra utiliser le[mode de compatibilité Office PPP](https://support.office.com/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).

<h3 id="activex-controls">Contrôles ActiveX</h3>

Comment prendre en charge la mise à l’échelle PPP dans les contrôles ActiveX dépend de si le contrôle dans une fenêtre ou sans fenêtre.

#### <a name="windowed-activex-controls"></a>Contrôles ActiveX dans une fenêtre

Les contrôles ActiveX dans une fenêtre reçoivent un message WM_SIZE chaque fois que le contrôle est redimensionné.  Lorsque cet événement est déclenché, le code gestionnaire d’événements peut d’appeler la fonction [GetDpiForWindow](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdpiforwindow) utilisant HWND du contrôle pour obtenir le PPP, calculer les différences de facteur échelle et ajuster en conséquence. 

L’exemple suivant permet au contrôle ActiveX basé sur MFC de répondre à l’événement **OnSize**. 

```cpp
void ChangeWindowFontDPI(HWND hWnd, UINT dpi) 
{ 
LOGFONT fontInfo1 = { 0 }; 
// Calculate the font height based on the DPI. 
fontInfo1.lfHeight = -MulDiv(DESIRED_HEIGHT, dpi, 72); 
fontInfo1.lfQuality = CLEARTYPE_QUALITY; 
wcscpy_s(fontInfo1.lfFaceName, DESIRED_FONT_NAME); 
 
::SendMessage(hWnd, WM_SETFONT, (WPARAM)::CreateFontIndirectW(&fontInfo1), TRUE); 
} 
 
BOOL CALLBACK CMainDialog::EnumChildProc(HWND hWnd, LPARAM lParam) 
{ 
CMainDialog* _this = (CMainDialog*) lParam; 
if (_this != nullptr) 
{ 
// Calculate the scale factor difference between the old and new DPI changes. 
double scale = (((double) _this->m_newDPI) /  
   (((double) _this->m_currentDPI) / 100.0)) / 100; 
 
RECT rect = {}; 
::GetWindowRect(hWnd, &rect); 
 
POINT pt = { rect.left, rect.top }; 
::ScreenToClient(::GetParent(hWnd), &pt); 
 
// Adjust the window based on the scale changes. 
::MoveWindow(hWnd, 
pt.x * scale, 
pt.y * scale, 
(rect.right - rect.left) * scale, 
(rect.bottom - rect.top) * scale, 
TRUE); 
 
ChangeWindowFontDPI(hWnd, _this->m_newDPI); 
return TRUE; 
} 
return FALSE; 
} 
 
void CMainDialog::OnSize(UINT nType, int cx, int cy) 
{ 
CDialog::OnSize(nType, cx, cy); 
 
// Get the new DPI and enumerate the child windows that will use that value. 
m_currentDPI = ::GetDpiForWindow(this->GetSafeHwnd()); 
::EnumChildWindows(this->GetSafeHwnd(), EnumChildProc, (LPARAM)this); 
} 
```

#### <a name="windowless-activex-controls"></a>Contrôles ActiveX sans fenêtre

Les contrôles ActiveX ne sont pas garantis d’avoir un HWND.  Quand un contrôle ActiveX est inséré sur une zone de document, il placé en mode Création.  Dans les applications Office, le conteneur d’hébergement renvoie 0 pour l’appel à hDC -> GetWindow() dans le :: OnDraw événement lorsque le contrôle est en mode Création.  Un PPP fiable ne peut pas être récupéré dans ce cas. 

Toutefois, lorsque le contrôle est en mode d’exécution, Office renverra HWND où le contrôle doit être affiché.  Dans ce cas, le développeur de contrôle peut appeler [GetDpiForWindow](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdpiforwindow) afin de recevoir les polices, l’échelle, contrôles PPP actuels et ainsi de suite. 

<h3 id="ribbon-extensibility">Extensibilité du ruban </h3>

Les rappels Office pour les contrôles de ruban personnalisés sont également une présence thread PPP de système PPP pris en compte.  Si votre solution attend une présence de thread PPP différente, vous devez implémenter un bloc de contexte pour configurer la présence de thread attendue. Pour plus d’informations, voir [Créer un bloc de contexte](#build-a-context-block-for-incoming-thread-calls).

<h3 id="ole">Serveurs et clients OLE</h3>

Lorsqu’un serveur OLE est hébergé dans un conteneur de client OLE, vous ne pouvez pas fournir d’informations PPP actuelles ni prises en charge. Cela peut provoquer des problèmes, car certaines combinaisons de modes mixtes de fenêtre parent à fenêtre enfant ne sont pas pris en charge par l’architecture actuelle de Windows. Si Word ou Excel détecte qu’il existe plusieurs moniteurs avec différentes échelles PPP, ils ne prennent pas en charge l’activation sur place. Votre serveur OLE s’activera en externe. Si vous rencontrez des problèmes avec les interactions de serveur OLE, l’utilisateur devra utiliser le [mode de compatibilité Office PPP](https://support.office.com/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).

<h3 id="web-add-ins">Compléments Office web</h3>

Les compléments Office créés à l’aide de l’API JavaScript Office s’exécutent à l’intérieur d’un contrôle de navigateur. Vous pouvez gérer la mise à l’échelle PPP à l’aide des mêmes techniques utilisées dans n’importe quelle conception d’applications web. Plusieurs ressources en ligne sont disponibles pour vous aider à créer une page web pour les écrans haute résolution.

## <a name="verify-that-your-solution-supports-dpi-scaling"></a>Vérifier que votre solution prend en charge la mise à l’échelle PPP

Une fois que vous avez mis à jour votre application pour prendre en charge la mise à l’échelle PPP, vous devez valider vos modifications dans un environnement mixte PPP. Vérifiez que votre code d’interface utilisateur répond correctement aux modifications PPP quand les fenêtres de votre solution sont déplacées d’un affichage à un autre ayant des valeurs PPP différentes. Pour plus d’informations sur les techniques de test de redimensionnement PPP, voir [Développement d’applications bureau haute résolution sur Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics).

Vous pouvez également trouver ces techniques supplémentaires utiles :

- Avec un ordinateur portable, vous pouvez configurer le moniteur principal à un moniteur externe, puis détacher l’ordinateur portable. Cela force le moniteur principal à aligner son affichage à celui de l’ordinateur portable.
- Utiliser l’open source [WinSpy ++ outil](https://github.com/BissetJ/winspy/releases) afin de déboguer. Vous pouvez l’utiliser pour afficher le paramètre de présence PPP de n’importe quelle fenêtre.
- Vous pouvez utiliser le bureau à distance pour tester plusieurs moniteurs sur un ordinateur distant en sélectionnant Utiliser tous mes moniteurs pour la session distante sous l’onglet Affichage, comme illustré dans la capture d’écran suivante.

![L’application de Connexion Bureau à distance montrant l’onglet Affichage, et sélectionnant Utiliser mes moniteurs pour la session distante.](./media/remote-desktop-use-all-monitors.png)

## <a name="see-also"></a>Voir aussi

### <a name="articles"></a>Articles

- [Le développement dPer-Monitor DPI-Aware application WPF fournit](https://docs.microsoft.com/windows/desktop/hidpi/declaring-managed-apps-dpi-aware) une vue d’ensemble générale et un guide pour l’écriture d’applications de bureau Win32. Bon nombre des techniques décrites dans cet article peuvent être appliquées aux solutions d’extensibilité Office.
- 
  [Mise à l’échelle PPP mode mixte et API PPP pris en compte](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-improvements-for-desktop-applications) a une liste d’API connexes à PPP.
- [Guie de développeur - Par moniteur PPP - Aperçu WPF](https://github.com/Microsoft/WPF-Samples/blob/master/PerMonitorDPI/Developer%20Guide%20-%20Per%20Monitor%20DPI%20-%20WPF%20Preview.docx) couvre le guide de développement d’application WPF pour créer des applications WPF PPP pris en compte.
- [Support technique Office pour l’affichage haute définition](https://support.office.com/article/Office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d) fournit des informations sur la manière dont un utilisateur peut définir Office afin d’optimiser pour assurer la compatibilité si votre solution Office n’est pas prise en charge correctement lorsque le PPP change.
- [Afficher les modifications de mise à l’échelle pour la Mise à jour anniversaire Windows 10](https://blogs.technet.microsoft.com/askcore/2016/08/16/display-scaling-changes-for-the-windows-10-anniversary-update/) est un billet de blog qui présente les modifications introduites avec la mise à jour anniversaire Windows 10. 
- [Gérer DPI_AWARENESS_CONTEXT](https://docs.microsoft.com/windows/desktop/hidpi/dpi-awareness-context) contient les détails de programme sur les valeurs et définitions de DPI_AWARENESS_CONTEXT.
- [Développement d’applications bureau PPP élevée sur Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#testing-your-changes) inclut des informations sur le test dans la section Testez vos modifications.

### <a name="code-samples"></a>Exemples de code

- [Exemple de présence PPP par fenêtre](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow)
- [Exemples de PPP dynamiques](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DynamicDPI)
- [Exemple WPF par moniteur pris en compte](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)
