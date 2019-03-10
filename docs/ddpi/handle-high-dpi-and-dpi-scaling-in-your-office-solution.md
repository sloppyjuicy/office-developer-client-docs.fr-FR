---
title: Gérer une résolution élevée et redimensionner la résolution dans votre solution Office
description: Mettre à jour votre solution Office tels que les volets de tâches personnalisés, ou les contrôles ActiveX, pour prendre en charge des moniteurs à haute résolution.
ms.date: 03/09/2019
localization_priority: Normal
ms.openlocfilehash: 7092b77a6c7cf56e3dafa0a4c893566778abf00b
ms.sourcegitcommit: c9720dd639f5c969f3cf6a324b84fadc57199370
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "30517401"
---
# <a name="handle-high-dpi-and-dpi-scaling-in-your-office-solution"></a><span data-ttu-id="cc932-103">Gérer une résolution élevée et redimensionner la résolution dans votre solution Office</span><span class="sxs-lookup"><span data-stu-id="cc932-103">Handle high DPI and DPI scaling in your Office solution</span></span>

<span data-ttu-id="cc932-104">De nombreuses configurations d’écran et d’ordinateur prennent désormais en charge une résolution élevée PPP (points par pouce) et peuvent mettre en contact plusieurs moniteurs de différentes tailles et densités exprimées en pixels.</span><span class="sxs-lookup"><span data-stu-id="cc932-104">Many computer and display configurations now support high DPI (dots-per-inch) resolutions, and can connect multiple monitors with different sizes and pixel densities.</span></span> <span data-ttu-id="cc932-105">Ceci nécessite que les applications s’ajustent quand l’utilisateur déplace l’application sur un moniteur avec une résolution différente ou modifie le niveau de zoom.</span><span class="sxs-lookup"><span data-stu-id="cc932-105">This requires applications to adjust when the user moves the app to a monitor with a different DPI, or changes the zoom level.</span></span> <span data-ttu-id="cc932-106">Les applications qui ne prennent pas en charge la mise à l’échelle PPP peuvent avoir un bon rendu sur moniteurs à faible PPP mais auront l’air étirées et floues sur un écran haute résolution.</span><span class="sxs-lookup"><span data-stu-id="cc932-106">Applications that don’t support DPI scaling might look fine on low DPI monitors, but will look stretched and blurry when shown on a high DPI monitor.</span></span> 

<span data-ttu-id="cc932-107">Les applications Office 2016, telles que Word et Excel, ont été mises à jour pour répondre aux modifications d’échelle.</span><span class="sxs-lookup"><span data-stu-id="cc932-107">Office 2016 applications, such as Word and Excel, have been updated to respond to changes in scale factor.</span></span> <span data-ttu-id="cc932-108">Toutefois, votre solution Office doit également répondre aux modifications pour dessiner correctement lorsque le PPP change.</span><span class="sxs-lookup"><span data-stu-id="cc932-108">However, your Office solution must also respond to changes to draw correctly when the DPI changes.</span></span> <span data-ttu-id="cc932-109">Cet article décrit comment Office prend en charge les PPP dynamiques et quelles opérations vous pouvez effectuer pour assurer la meilleure expérience d’affichage pour votre solution extensibilité Office pour gérer le redimensionnement PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-109">This article describes how Office supports dynamic DPI, and what steps you can take to ensure the best viewing experience for your Office extensibility solution to handle DPI scaling.</span></span> 

## <a name="dpi-scaling-symptoms-in-your-solution"></a><span data-ttu-id="cc932-110">Symptômes de redimensionnement PPP dans votre solution</span><span class="sxs-lookup"><span data-stu-id="cc932-110">DPI scaling symptoms in your solution</span></span>

<span data-ttu-id="cc932-111">Windows applique le redimensionnement PPP lorsqu’une application est déplacée d’un type d’affichage à un autre avec une résolution différente.</span><span class="sxs-lookup"><span data-stu-id="cc932-111">Windows applies DPI scaling when an application is moved from one display to another display with a different DPI.</span></span> <span data-ttu-id="cc932-112">Cela se produit lorsque vous faites glisser une application vers un autre écran ou utilisez l’ancrage de votre ordinateur portable.</span><span class="sxs-lookup"><span data-stu-id="cc932-112">This happens in scenarios such as dragging an application to a different monitor or docking your laptop.</span></span> <span data-ttu-id="cc932-113">Si votre solution Office est affectée négativement par le redimensionnement PPP, vous pouvez constater un ou plusieurs des symptômes suivants :</span><span class="sxs-lookup"><span data-stu-id="cc932-113">If your Office solution is adversely affected by DPI scaling, you will see one or more of the following symptoms:</span></span>

- <span data-ttu-id="cc932-114">Les fenêtres apparaissent au mauvais emplacement ou ont une taille incorrecte.</span><span class="sxs-lookup"><span data-stu-id="cc932-114">The windows draw in the wrong location or have incorrect sizing.</span></span>
- <span data-ttu-id="cc932-115">Les éléments tels que les boutons et étiquettes apparaissent dans un emplacement incorrect dans la fenêtre de votre solution.</span><span class="sxs-lookup"><span data-stu-id="cc932-115">Elements such as buttons and labels appear in the wrong location in your solution’s window.</span></span>
- <span data-ttu-id="cc932-116">Les polices et images sont trop petites, trop volumineuses ou à un emplacement incorrect.</span><span class="sxs-lookup"><span data-stu-id="cc932-116">Fonts and images appear too small, too large or in the wrong location.</span></span>

<span data-ttu-id="cc932-117">Les types suivants de solutions Office peuvent être affectés par la mise à l’échelle PPP :</span><span class="sxs-lookup"><span data-stu-id="cc932-117">The following types of Office solutions can be affected by DPI scaling:</span></span>

- <span data-ttu-id="cc932-118">Compléments VSTO</span><span class="sxs-lookup"><span data-stu-id="cc932-118">VSTO Add-ins</span></span>
- <span data-ttu-id="cc932-119">Volets des tâches personnalisés</span><span class="sxs-lookup"><span data-stu-id="cc932-119">Custom task panes</span></span>
- <span data-ttu-id="cc932-120">Compléments COM</span><span class="sxs-lookup"><span data-stu-id="cc932-120">COM Add-ins</span></span>
- <span data-ttu-id="cc932-121">Contrôles ActiveX</span><span class="sxs-lookup"><span data-stu-id="cc932-121">ActiveX controls</span></span>
- <span data-ttu-id="cc932-122">Extensions de ruban</span><span class="sxs-lookup"><span data-stu-id="cc932-122">Ribbon extensions</span></span>
- <span data-ttu-id="cc932-123">Serveurs OLE</span><span class="sxs-lookup"><span data-stu-id="cc932-123">Ole servers</span></span>
- <span data-ttu-id="cc932-124">Compléments Office web</span><span class="sxs-lookup"><span data-stu-id="cc932-124">Office web add-ins</span></span>

## <a name="windows-dpi-awareness-modes"></a><span data-ttu-id="cc932-125">Modes de présence PPP Windows</span><span class="sxs-lookup"><span data-stu-id="cc932-125">Windows DPI awareness modes</span></span>

<span data-ttu-id="cc932-126">Dans cet article, nous allons faire référence aux modes de sensibilisation PPP que Windows prend en charge.</span><span class="sxs-lookup"><span data-stu-id="cc932-126">Throughout this article we’ll refer to the DPI awareness modes that Windows supports.</span></span> <span data-ttu-id="cc932-127">Chaque mode de présence PPP prend en charge différentes fonctionnalités, comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="cc932-127">Each DPI awareness mode supports different capabilities, as described in the following table.</span></span> <span data-ttu-id="cc932-128">Il s’agit d’une description simplifiée des modes afin d’expliquer comment les solutions Office les prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="cc932-128">This is a simplified description of the modes to explain how Office solutions support them.</span></span> <span data-ttu-id="cc932-129">Pour plus d’informations sur les modes de présence PPP, voir [Développement d’applications bureau haute résolution sur Windows](https://docs.microsoft.com/en-us/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows).</span><span class="sxs-lookup"><span data-stu-id="cc932-129">For more information about the DPI awareness modes, see [High DPI Desktop Application Development on Windows](https://docs.microsoft.com/en-us/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows).</span></span>

|<span data-ttu-id="cc932-130">Mode</span><span class="sxs-lookup"><span data-stu-id="cc932-130">Mode</span></span>  |<span data-ttu-id="cc932-131">Description</span><span class="sxs-lookup"><span data-stu-id="cc932-131">Description</span></span>  |<span data-ttu-id="cc932-132">Lorsque la résolution change</span><span class="sxs-lookup"><span data-stu-id="cc932-132">When DPI changes</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="cc932-133">Système PPP ignoré</span><span class="sxs-lookup"><span data-stu-id="cc932-133">DPI unaware</span></span>     |    <span data-ttu-id="cc932-134">L’application s’affiche toujours comme si elle est sur une résolution de valeur 96.</span><span class="sxs-lookup"><span data-stu-id="cc932-134">Application always renders as if it is on a display with a DPI value of 96.</span></span>     |    <span data-ttu-id="cc932-135">L’application est étirée bitmap à la taille attendue sur l’affichage principal et secondaire.</span><span class="sxs-lookup"><span data-stu-id="cc932-135">Application is bitmap stretched to expected size on primary and secondary displays.</span></span>    |
|<span data-ttu-id="cc932-136">Système PPP pris en compte</span><span class="sxs-lookup"><span data-stu-id="cc932-136">System DPI aware</span></span>     |   <span data-ttu-id="cc932-137">L’application détecte la résolution du moniteur principal connecté à Windows, mais ne peut pas répondre aux modifications PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-137">Application detects the DPI of the primary connected monitor at Windows login but cannot respond to DPI changes.</span></span> <span data-ttu-id="cc932-138">Pour plus d’informations, voir la section[Configurer Windows pour corriger les applications floues](#Configure-Windows-to-fix-blurry-apps) de cet article.</span><span class="sxs-lookup"><span data-stu-id="cc932-138">For more information, see [Configure Windows to fix blurry apps](#Configure-Windows-to-fix-blurry-apps) section in this article.</span></span>      |     <span data-ttu-id="cc932-139">L’application est étirée bitmap lorsqu’elle est déplacée vers un nouvel affichage avec une résolution différente.</span><span class="sxs-lookup"><span data-stu-id="cc932-139">Application is bitmap stretched when moved to a new display with a different DPI.</span></span>    |
|<span data-ttu-id="cc932-140">Par moniteur PPP pris en compte</span><span class="sxs-lookup"><span data-stu-id="cc932-140">Per Monitor DPI aware</span></span>     |    <span data-ttu-id="cc932-141">L’application est capable de s’afficher correctement d’elle-même lorsque le PPP change.</span><span class="sxs-lookup"><span data-stu-id="cc932-141">Application is capable of redrawing itself correctly when the DPI changes.</span></span>     |    <span data-ttu-id="cc932-142">Windows envoie des notifications PPP aux fenêtres de niveau supérieur dans l’application, de sorte qu’elle peut ajuster son affichage en cas de modification de la résolution.</span><span class="sxs-lookup"><span data-stu-id="cc932-142">Windows will send DPI notifications to top-level windows in the application so that it can redraw when the DPI changes.</span></span>     |
|<span data-ttu-id="cc932-143">Par moniteur v2</span><span class="sxs-lookup"><span data-stu-id="cc932-143">Per Monitor v2</span></span>     |   <span data-ttu-id="cc932-144">L’application est capable de s’afficher correctement d’elle-même lorsque le PPP change.</span><span class="sxs-lookup"><span data-stu-id="cc932-144">Application is capable of redrawing itself correctly when the DPI changes.</span></span>      |        <span data-ttu-id="cc932-145">Windows envoie des notifications PPP aux fenêtres de niveau supérieur et aux fenêtres enfants dans l’application, de sorte qu’elle peut ajuster son affichage en cas de modification de la résolution.</span><span class="sxs-lookup"><span data-stu-id="cc932-145">Windows will send DPI notifications to both top-level and child windows so that the application can redraw when the DPI changes.</span></span> |

## <a name="how-office-supports-dpi-scaling"></a><span data-ttu-id="cc932-146">Comment Office prend en charge la mise à l’échelle PPP</span><span class="sxs-lookup"><span data-stu-id="cc932-146">How Office supports DPI scaling</span></span>

<span data-ttu-id="cc932-147">Le facteur le plus significatif dans la détermination de comment votre solution Office peut gérer la mise à l’échelle PPP est si votre solution est une fenêtre de niveau supérieur ou une fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="cc932-147">The most significant factor in determining how your Office solution can handle DPI scaling is whether your solution is a top-level window, or a child window.</span></span> <span data-ttu-id="cc932-148">L’image suivante montre quelques exemples de solutions Office opérationnelles en tant que fenêtres de niveau supérieur ou enfants, et quel mode de présence PPP elles utilisent sur la mise à jour Windows avril 2018 (1803) et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="cc932-148">The following picture shows a few examples of Office solutions running as top-level or child windows, and which DPI awareness mode they will use on Windows April 2018 Update (1803) and later.</span></span>

![Excel hébergeant un contrôle ActiveX et un volet de tâches personnalisé en tant que fenêtre enfant.](./media/office-dpi-awareness-for-solution-types.png)

<span data-ttu-id="cc932-152">Dans cette image :</span><span class="sxs-lookup"><span data-stu-id="cc932-152">In this image:</span></span>
- <span data-ttu-id="cc932-153">La fenêtre de niveau supérieur COM/VSTO est Par moniteur PPP pris en compte.</span><span class="sxs-lookup"><span data-stu-id="cc932-153">The COM/VSTO top-level window is Per Monitor DPI aware.</span></span>
- <span data-ttu-id="cc932-154">La fenêtre enfant de contrôle ActiveX est Système PPP pris en compte.</span><span class="sxs-lookup"><span data-stu-id="cc932-154">The ActiveX control child window is System DPI aware.</span></span>
- <span data-ttu-id="cc932-155">La fenêtre de niveau supérieur Office est Par moniteur PPP pris en compte.</span><span class="sxs-lookup"><span data-stu-id="cc932-155">The Office top-level window is Per Monitor DPI aware.</span></span>
- <span data-ttu-id="cc932-156">La fenêtre enfant de volet de tâches personnalisé est Système PPP pris en compte.</span><span class="sxs-lookup"><span data-stu-id="cc932-156">The custom task pane child window is System DPI aware.</span></span>

## <a name="managing-thread-dpi-context"></a><span data-ttu-id="cc932-157">La gestion de contexte de thread PPP</span><span class="sxs-lookup"><span data-stu-id="cc932-157">Managing thread DPI context</span></span>

<span data-ttu-id="cc932-158">Lorsque l’application Office hôte démarre, son thread principal est exécuté en contexte Par moniteur PPP pris en compte.</span><span class="sxs-lookup"><span data-stu-id="cc932-158">When the host Office app starts, its main thread runs in Per Monitor DPI aware context.</span></span> <span data-ttu-id="cc932-159">Lorsque votre code de solution crée des threads ou reçoit des appels à partir d’Office, vous devez gérer le contexte PPP du thread.</span><span class="sxs-lookup"><span data-stu-id="cc932-159">When your solution code creates threads, or receives calls from Office, you need to manage the thread DPI context.</span></span>

### <a name="creating-new-threads-with-the-correct-dpi-context"></a><span data-ttu-id="cc932-160">Création de nouveaux threads avec le contexte PPP correct</span><span class="sxs-lookup"><span data-stu-id="cc932-160">Creating new threads with the correct DPI context</span></span>

<span data-ttu-id="cc932-161">Si votre solution crée des threads supplémentaires, Office obligent les threads à utiliser un contexte Par moniteur PPP pris en compte.</span><span class="sxs-lookup"><span data-stu-id="cc932-161">If your solution creates additional threads, Office will force the threads into Per Monitor DPI aware context.</span></span> <span data-ttu-id="cc932-162">Si votre code attend un contexte différent, vous devez utiliser la fonction [SetThreadDpiAwarenessContext](https://docs.microsoft.com/en-us/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) pour définir la présence de thread PPP prévue.</span><span class="sxs-lookup"><span data-stu-id="cc932-162">If your code expects a different context, you need to use the [SetThreadDpiAwarenessContext](https://docs.microsoft.com/en-us/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) function to set the expected thread DPI awareness.</span></span> 

### <a name="build-a-context-block-for-incoming-thread-calls"></a><span data-ttu-id="cc932-163">Créer un bloc de contexte pour les appels thread entrants </span><span class="sxs-lookup"><span data-stu-id="cc932-163">Build a context block for incoming thread calls</span></span>

![Diagramme montrant le bloc de contexte dans l’application Office passant le thread à un contexte Système pris en compte sur les appels à votre fenêtre de niveau supérieur.](./media/thread-dpi-awareness-context-block.png)

<span data-ttu-id="cc932-165">Votre solution interagit avec son application Office hôte, donc vous aurez des appels entrants pour votre solution à partir d’Office, tels que des rappels d’événement.</span><span class="sxs-lookup"><span data-stu-id="cc932-165">Your solution will interact with its host Office app, so you will have incoming calls to your solution from Office such as event callbacks.</span></span> <span data-ttu-id="cc932-166">Lorsque Office appelle votre solution, celui-ci comporte un bloc de contexte qui force le contexte de thread en contexte Système PPP pris en compte.</span><span class="sxs-lookup"><span data-stu-id="cc932-166">When Office calls your solution, it has a context block that forces the thread context to be in System DPI Aware context.</span></span> <span data-ttu-id="cc932-167">Vous devez modifier le contexte du thread pour qu’il soit conforme à la présence de résolution de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cc932-167">You must change the thread context to match the DPI awareness of your window.</span></span> <span data-ttu-id="cc932-168">Vous pouvez implémenter un bloc de contexte similaire pour basculer le contexte du thread sur les appels entrants.</span><span class="sxs-lookup"><span data-stu-id="cc932-168">You can implement a similar context block to switch the thread context on incoming calls.</span></span> <span data-ttu-id="cc932-169">Utilisez la fonction [SetThreadDpiAwarenessContext](https://docs.microsoft.com/en-us/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) pour modifier le contexte pour correspondre au contexte de votre fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cc932-169">Use the [SetThreadDpiAwarenessContext](https://docs.microsoft.com/en-us/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) function to change the context to match your window context.</span></span> 

> [!NOTE]
> <span data-ttu-id="cc932-170">Votre bloc de contexte doit restaurer le contexte du thread PPP d’origine avant d’appeler d’autres composants en dehors de votre code de solution.</span><span class="sxs-lookup"><span data-stu-id="cc932-170">Your context block should restore the original DPI thread context before calling other components outside of your solution code.</span></span>

#### <a name="managed-code-context-block"></a><span data-ttu-id="cc932-171">Gérer le bloc de contexte code</span><span class="sxs-lookup"><span data-stu-id="cc932-171">Managed code context block</span></span>

<span data-ttu-id="cc932-172">L’exemple de code suivant montre comment créer votre propre bloc de contexte.</span><span class="sxs-lookup"><span data-stu-id="cc932-172">The following example code shows how to construct your own context block.</span></span>

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

            public static DPI_AWARENESS_CONTEXT operator -(DPI_AWARENESS_CONTEXT context, long value)
            {
                return (IntPtr)(context.value.ToInt64() - value);
            }
            public static DPI_AWARENESS_CONTEXT operator -(DPI_AWARENESS_CONTEXT context, int value)
            {
                return (IntPtr)(context.value.ToInt32() - value);
            }

            public static bool operator ==(DPI_AWARENESS_CONTEXT context1, DPI_AWARENESS_CONTEXT context2)
            {
                return context1.value == context2;
            }
            public static bool operator !=(DPI_AWARENESS_CONTEXT context1, DPI_AWARENESS_CONTEXT context2)
            {
                return context1.value != context2;
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

            public override string ToString()
            {
                if (this.value == DPI_AWARENESS_CONTEXT_UNAWARE)
                {
                    return "Unaware";
                }
                if (this.value == DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)
                {
                    return "System Aware";
                }
                if (this.value == DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)
                {
                    return "Per Monitor Aware";
                }
                if (this.value == DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)
                {
                    return "Per Monitor Aware V2";
                }
                return "Unknown";
            }
        }

        private static DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_HANDLE = IntPtr.Zero;

        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_INVALID = IntPtr.Zero;
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_UNAWARE = DPI_AWARENESS_CONTEXT_HANDLE - 1;
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_SYSTEM_AWARE = DPI_AWARENESS_CONTEXT_HANDLE - 2;
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE = DPI_AWARENESS_CONTEXT_HANDLE - 3;
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 = DPI_AWARENESS_CONTEXT_HANDLE - 4;

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

#### <a name="native-code-context-block"></a><span data-ttu-id="cc932-173">Bloc de contexte code natif</span><span class="sxs-lookup"><span data-stu-id="cc932-173">Native code context block</span></span>

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
<h2 id="top-level-window-management"><span data-ttu-id="cc932-174">Gestion de fenêtre de niveau supérieur</span><span class="sxs-lookup"><span data-stu-id="cc932-174">Top-level window management</span></span></h2>

<span data-ttu-id="cc932-175">Lors du démarrage des applications Office, un appel est effectué à [SetThreadDpiAwarenessContext](https://docs.microsoft.com/en-us/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) comme DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE.</span><span class="sxs-lookup"><span data-stu-id="cc932-175">When Office applications start, a call is made to [SetThreadDpiAwarenessContext](https://docs.microsoft.com/en-us/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) as DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE.</span></span> <span data-ttu-id="cc932-176">Dans ce contexte, les modifications PPP sont envoyées à HWND de n’importe quelle fenêtre de niveau supérieur dans le processus en cours d’exécution avec moniteur PPP pris en compte.</span><span class="sxs-lookup"><span data-stu-id="cc932-176">In this context, DPI changes are sent to the HWND of any top-level windows in the process that are running as Per Monitor DPI aware.</span></span> <span data-ttu-id="cc932-177">Les fenêtres de niveau supérieur sont les fenêtres d’application Office, et toute autre fenêtre de niveau supérieur créée par votre solution.</span><span class="sxs-lookup"><span data-stu-id="cc932-177">Top-level windows are the Office application window, and any additional top-level windows created by your solution.</span></span> <span data-ttu-id="cc932-178">Lorsqu’une application Office est déplacée vers un nouvel affichage, elle reçoit une notification afin qu’elle puisse se mettre à l’échelle dynamiquement et s’afficher correctement dans la résolution du nouvel affichage.</span><span class="sxs-lookup"><span data-stu-id="cc932-178">When an Office application is moved to a new display, it gets notified so that it can dynamically scale and draw correctly in the DPI of the new display.</span></span> <span data-ttu-id="cc932-179">Votre solution Office pouvez créer des fenêtres de niveau supérieur qui se trouvent dans n’importe quel mode de présence PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-179">Your Office solution can create top-level windows that are in any DPI awareness mode.</span></span> <span data-ttu-id="cc932-180">Vos fenêtres de niveau supérieur peuvent également répondre aux modifications PPP en écoutant les messages Windows pour les modifications.</span><span class="sxs-lookup"><span data-stu-id="cc932-180">Your top-level windows can also respond to DPI changes by listening to Windows messages for the changes.</span></span>

<span data-ttu-id="cc932-181">Si vous créez des fenêtres enfants apparentées à votre fenêtre de niveau supérieur, vous pouvez également les définir sur n’importe quel mode de présence PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-181">If you create child windows that are parented to your top-level window, you can also set them to any DPI awareness mode.</span></span> <span data-ttu-id="cc932-182">Toutefois, si vous utilisez le mode Par moniteur PPP pris en compte, vos fenêtres enfant ne recevront pas les notifications de modification PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-182">However, if you use Per Monitor DPI aware mode, your child windows will not receive DPI change notifications.</span></span>  <span data-ttu-id="cc932-183">Pour plus d’informations sur les modes de présence PPP Windows, voir [Développement d’applications bureau haute résolution sur Windows](https://docs.microsoft.com/en-us/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows).</span><span class="sxs-lookup"><span data-stu-id="cc932-183">For more information about Windows DPI awareness modes, see [High DPI Desktop Application Development on Windows](https://docs.microsoft.com/en-us/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows).</span></span>

## <a name="child-window-management"></a><span data-ttu-id="cc932-184">Gestion de fenêtre enfant</span><span class="sxs-lookup"><span data-stu-id="cc932-184">Child window management</span></span>

<span data-ttu-id="cc932-185">Lorsque vous travaillez avec des contrôles ActiveX et volets de tâches personnalisés, Office crée la fenêtre enfant pour votre solution.</span><span class="sxs-lookup"><span data-stu-id="cc932-185">When working with ActiveX controls and custom task panes, Office creates the child window for your solution.</span></span> <span data-ttu-id="cc932-186">Vous pouvez créer des fenêtres enfants supplémentaires, mais vous devez tenir compte de la présence PPP de la fenêtre parent.</span><span class="sxs-lookup"><span data-stu-id="cc932-186">You can create additional child windows, but you have to be aware of the parent window DPI awareness.</span></span> <span data-ttu-id="cc932-187">Office est exécuté en mode de présence Per moniteur PPP, ce qui signifie qu’aucune fenêtre enfant dans votre solution ne recevra pas de notifications de modification PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-187">Office runs in Per Monitor DPI awareness mode, which means any child windows in your solution will not get DPI change notifications.</span></span> <span data-ttu-id="cc932-188">Uniquement le mode Par moniteur v2 prend en charge l’envoi de modifications PPP aux fenêtres enfant (Office ne prend pas en charge Par moniteur v2).</span><span class="sxs-lookup"><span data-stu-id="cc932-188">Only Per Monitor v2 mode supports sending DPI changes to child windows (Office does not support Per Monitor v2).</span></span> <span data-ttu-id="cc932-189">Toutefois, pour les contrôles ActiveX, il existe une solution de contournement.</span><span class="sxs-lookup"><span data-stu-id="cc932-189">However, for ActiveX controls, there is a workaround.</span></span> <span data-ttu-id="cc932-190">Pour plus d’informations, voir la section [Contrôles ActiveX](#activex-controls) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="cc932-190">For more information, see the [ActiveX controls](#activex-controls) section later in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="cc932-191">Si votre fenêtre enfant crée une fenêtre de niveau supérieur, vous pouvez utiliser n’importe quel mode de présence PPP pour la nouvelle fenêtre de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="cc932-191">If your child window creates a top-level window, you can use any DPI awareness mode for the new top-level window.</span></span> <span data-ttu-id="cc932-192">Pour plus d’informations sur la gestion des fenêtres de niveau supérieur, voir la section [Gestion de la fenêtre de niveau supérieur](#top-level-window-management) de cet article.</span><span class="sxs-lookup"><span data-stu-id="cc932-192">For more information about managing top-level windows, see the [Top-level window management](#top-level-window-management) section in this article.</span></span>

<span data-ttu-id="cc932-193">Vous verrez deux différents modes PPP appliqués à la fenêtre enfant, selon la version d’Office Windows 10 en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="cc932-193">You will see two different DPI modes applied to your child window, depending on which version of Windows 10 Office is running on.</span></span>

### <a name="office-dpi-behavior-on-windows-fall-creators-update-1709"></a><span data-ttu-id="cc932-194">Comportement Office PPP sur Windows Fall Creators Update (1709)</span><span class="sxs-lookup"><span data-stu-id="cc932-194">Office DPI behavior on Windows Fall Creators Update (1709)</span></span>

<span data-ttu-id="cc932-195">Étant donné que les applications Office utilisent le mode de présence par moniteur, les fenêtres enfants de votre solution seront également créées en mode de présence Per moniteur PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-195">Because Office apps use Per Monitor awareness mode, your solution’s child windows will also be created in Per Monitor DPI awareness mode.</span></span> <span data-ttu-id="cc932-196">Cela signifie que Windows attend de votre solution qu’elle se mette à jour lorsqu’elle s’affiche dans un nouveau PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-196">This means Windows expects your solution to update when drawing in a new DPI.</span></span>  <span data-ttu-id="cc932-197">Étant donné que la fenêtre ne peut pas recevoir de notifications de modification PPP, l’interface utilisateur de votre solution peut être incorrecte.</span><span class="sxs-lookup"><span data-stu-id="cc932-197">Because your window cannot get DPI change notifications, your solution’s UI might be incorrect.</span></span> 

![Diagramme montrant les fenêtres enfants en cours d’exécution dans un contexte Par moniteur PPP pris en compte sur Windows Fall Creators Update (1709).](./media/office-dpi-behavior-on-windows-fall-creators-update.png)

### <a name="office-dpi-behavior-on-windows-april-2018-update-1803"></a><span data-ttu-id="cc932-199">Comportement Office PPP sur Mise à jour Windows avril 2018 (1803)</span><span class="sxs-lookup"><span data-stu-id="cc932-199">Office DPI behavior on Windows April 2018 Update (1803)</span></span>

<span data-ttu-id="cc932-200">Avec la mise à jour Windows avril 2018 (1803) et versions ultérieures, le comportement d’hébergement Office PPP utilise la mise à l’échelle PPP en mode mixte pour certains scénarios.</span><span class="sxs-lookup"><span data-stu-id="cc932-200">With Windows April 2018 (1803) update and later, The Office DPI hosting behavior uses mixed-mode DPI scaling for some scenarios.</span></span> <span data-ttu-id="cc932-201">Cela permet aux fenêtres de système PPP pris en compte d’être liées aux fenêtres Office configurées sur Par moniteur PPP pris en compte.</span><span class="sxs-lookup"><span data-stu-id="cc932-201">This allows System DPI Aware windows to be parented to Office windows set to Per Monitor DPI aware.</span></span> <span data-ttu-id="cc932-202">Cela permet de garantir une meilleure compatibilité lorsque la résolution change lorsque les fenêtres sont étirées bitmap.</span><span class="sxs-lookup"><span data-stu-id="cc932-202">This helps to ensure improved compatibility when the DPI changes when the windows are bitmap stretched.</span></span> <span data-ttu-id="cc932-203">Les fenêtres peuvent toujours être floues en raison de l’étirement bitmap.</span><span class="sxs-lookup"><span data-stu-id="cc932-203">The windows might still be blurry from the bitmap stretching.</span></span>

![Diagramme montrant les fenêtres enfants en cours d’exécution dans un contexte Par système PPP pris en compte sur Windows mise à jour avril 2018 (1803).](./media/office-dpi-behavior-on-windows-april-2018-update.png)

<span data-ttu-id="cc932-205">Lorsque vous créez nouveau fenêtre enfant, assurez-vous qu’elles correspondent à la résolution de présence de leur fenêtre parent.</span><span class="sxs-lookup"><span data-stu-id="cc932-205">When you create new child windows, be sure they match the DPI awareness of their parent window.</span></span> <span data-ttu-id="cc932-206">Vous pouvez utiliser la fonction[GetWindowdpiAwarenessContext](https://docs.microsoft.com/en-us/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext) pour obtenir la résolution de présence de la fenêtre parent.</span><span class="sxs-lookup"><span data-stu-id="cc932-206">You can use the [GetWindowdpiAwarenessContext](https://docs.microsoft.com/en-us/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext) function to get the DPI awareness of the parent window.</span></span> <span data-ttu-id="cc932-207">Pour plus d’informations sur la cohérence de présence PPP, voir la section « Réinitialisation forcée de présence à l’échelle de processus PPP » dans [Développement d’applications bureau pour haute résolution sur Windows](https://docs.microsoft.com/en-us/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics).</span><span class="sxs-lookup"><span data-stu-id="cc932-207">For more information about DPI awareness consistency, see the “Forced reset of process-wide DPI awareness” section in [High DPI Desktop Application Development on Windows](https://docs.microsoft.com/en-us/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics).</span></span>

> [!NOTE]
> <span data-ttu-id="cc932-208">Vous ne pouvez pas dépendre de la présence de processus PPP car cela peut renvoyer [PROCESS_SYSTEM_DPI_AWARE](https://msdn.microsoft.com/en-us/library/windows/desktop/dn280512(v=vs.85).aspx) même lorsque le contexte de présence du thread principal PPP de l’application est [DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE](https://docs.microsoft.com/en-us/windows/desktop/hidpi/dpi-awareness-context).</span><span class="sxs-lookup"><span data-stu-id="cc932-208">You can’t rely on the Process DPI Awareness as it might return [PROCESS_SYSTEM_DPI_AWARE](https://msdn.microsoft.com/en-us/library/windows/desktop/dn280512(v=vs.85).aspx) even when the application main thread DPI awareness context is [DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE](https://docs.microsoft.com/en-us/windows/desktop/hidpi/dpi-awareness-context).</span></span> <span data-ttu-id="cc932-209">Utilisez la fonction [GetThreadDpiAwarenessContext](https://docs.microsoft.com/en-us/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext) pour obtenir le contexte de présence du thread PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-209">Use the [GetThreadDpiAwarenessContext](https://docs.microsoft.com/en-us/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext) function to get the thread DPI awareness context.</span></span>

## <a name="office-and-windows-dpi-compatibility-settings"></a><span data-ttu-id="cc932-210">Paramètres de compatibilité Office et Windows PPP</span><span class="sxs-lookup"><span data-stu-id="cc932-210">Office and Windows DPI compatibility settings</span></span>

<span data-ttu-id="cc932-211">Lorsque les utilisateurs rencontrent des compléments ou des solutions qui ne sont pas affichés correctement, certains paramètres de compatibilité peuvent vous aider à corriger le problème.</span><span class="sxs-lookup"><span data-stu-id="cc932-211">When users encounter add-ins or solutions that are not rendering correctly, some compatibility settings can help correct the problem.</span></span>

<h3 id="office-compatibility"><span data-ttu-id="cc932-212">Configurer Office pour optimiser la compatibilité</span><span class="sxs-lookup"><span data-stu-id="cc932-212">Configure Office to optimize for compatibility</span></span></h3>

<span data-ttu-id="cc932-213">Office a défini un paramètre pour optimiser la compatibilité lors de la transition vers différentes échelles PPP sur différents écrans.</span><span class="sxs-lookup"><span data-stu-id="cc932-213">Office has a setting to optimize for compatibility when moving to different DPI scales on different screens.</span></span> <span data-ttu-id="cc932-214">Le mode de compatibilité désactive la mise à l’échelle PPP afin que tout le contenu dans Office soit étiré bitmap lors du déplacement vers un affichage utilisant une échelle PPP différente.</span><span class="sxs-lookup"><span data-stu-id="cc932-214">The compatibility mode disables DPI scaling so that everything in Office is bitmap stretched when moved to a display using different DPI scaling.</span></span> 

<span data-ttu-id="cc932-215">Le mode de compatibilité force Office à s’exécuter en mode système PPP pris en compte.</span><span class="sxs-lookup"><span data-stu-id="cc932-215">The compatibility mode forces Office to run in System DPI aware mode.</span></span> <span data-ttu-id="cc932-216">Cela amène les fenêtres d’application à un étirement bitmap et peut avoir un aspect flou comme effet secondaire.</span><span class="sxs-lookup"><span data-stu-id="cc932-216">This causes application windows to bitmap stretch and can have a side effect of a blurry appearance.</span></span> <span data-ttu-id="cc932-217">Votre solution Office ne peut pas contrôler ce paramètre, car l’utilisateur choisit celui-ci.</span><span class="sxs-lookup"><span data-stu-id="cc932-217">Your Office solution cannot control this setting because the user chooses it.</span></span> <span data-ttu-id="cc932-218">Utiliser le mode de compatibilité d’affichage permet de résoudre la plupart des problèmes d’apparence.</span><span class="sxs-lookup"><span data-stu-id="cc932-218">Using the display compatibility mode solves most drawing problems.</span></span> <span data-ttu-id="cc932-219">Pour plus d’informations, voir [Support Office pour l’affichage haute définition](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span><span class="sxs-lookup"><span data-stu-id="cc932-219">For more information, see [Office support for high definition displays](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span></span> 

### <a name="configure-windows-to-fix-blurry-apps"></a><span data-ttu-id="cc932-220">Configurez Windows pour résoudre les application floues</span><span class="sxs-lookup"><span data-stu-id="cc932-220">Configure Windows to fix blurry apps</span></span>

<span data-ttu-id="cc932-221">Windows 10 (Version 1803) et versions suivantes ont défini un paramètre pour corriger les applications afin qu’elles ne soient pas floues.</span><span class="sxs-lookup"><span data-stu-id="cc932-221">Windows 10 (Version 1803) and later has a setting to fix apps so they’re not blurry.</span></span> <span data-ttu-id="cc932-222">Il s’agit d’un autre paramètre à essayer si votre solution n’est pas affichée correctement.</span><span class="sxs-lookup"><span data-stu-id="cc932-222">This is another setting to try if your solution is not rendering correctly.</span></span> <span data-ttu-id="cc932-223">Votre solution Office ne peut pas contrôler ce paramètre, car l’utilisateur choisit celui-ci.</span><span class="sxs-lookup"><span data-stu-id="cc932-223">Your Office solution cannot control this setting because the user chooses it.</span></span> <span data-ttu-id="cc932-224">Pour plus d’informations, voir [Corriger les applications qui s’affichent floues dans Windows 10](https://support.microsoft.com/en-us/help/4091364/windows-10-fix-blurry-apps).</span><span class="sxs-lookup"><span data-stu-id="cc932-224">For more information, see [Fix apps that appear blurry in Windows 10](https://support.microsoft.com/en-us/help/4091364/windows-10-fix-blurry-apps).</span></span>

## <a name="how-to-support-dpi-scaling-in-your-solution"></a><span data-ttu-id="cc932-225">Comment prendre en charge le redimensionnement PPP dans votre solution</span><span class="sxs-lookup"><span data-stu-id="cc932-225">How to support DPI scaling in your solution</span></span>

<span data-ttu-id="cc932-226">Certaines solutions peuvent recevoir et répondre aux modifications PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-226">Some solutions can receive and respond to DPI changes.</span></span> <span data-ttu-id="cc932-227">Certaines ont une solution de contournement si elles ne peuvent pas recevoir des notifications.</span><span class="sxs-lookup"><span data-stu-id="cc932-227">Some have a workaround if they cannot receive notifications.</span></span> <span data-ttu-id="cc932-228">Le tableau suivant répertorie les détails pour chaque type de solution.</span><span class="sxs-lookup"><span data-stu-id="cc932-228">The following table lists the details for each solution type.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="cc932-229">Type de solution</span><span class="sxs-lookup"><span data-stu-id="cc932-229">Solution Type</span></span></th>
            <th><span data-ttu-id="cc932-230">Type de fenêtre</span><span class="sxs-lookup"><span data-stu-id="cc932-230">Window type</span></span></th>
            <th><span data-ttu-id="cc932-231">Peut répondre au redimensionnement PPP</span><span class="sxs-lookup"><span data-stu-id="cc932-231">Can respond to DPI scaling</span></span></th>
            <th><span data-ttu-id="cc932-232">Plus de détails</span><span class="sxs-lookup"><span data-stu-id="cc932-232">More details</span></span></th>
        </tr>
    </thead>
<tbody>
    <tr>
        <td rowspan="2"><span data-ttu-id="cc932-233"><a href="#vsto-add-ins">Complément VSTO</a></span><span class="sxs-lookup"><span data-stu-id="cc932-233"><a href="#vsto-add-ins">VSTO Add-in</a></span></span></td>
        <td><span data-ttu-id="cc932-234">Niveau supérieur et descendants</span><span class="sxs-lookup"><span data-stu-id="cc932-234">Top and its descendants</span></span></td>
        <td><span data-ttu-id="cc932-235">Oui</span><span class="sxs-lookup"><span data-stu-id="cc932-235">Yes</span></span></td>
        <td><span data-ttu-id="cc932-236">Voir <a href="#vsto-add-ins">Conseils complément VSTO</a>.</span><span class="sxs-lookup"><span data-stu-id="cc932-236">See <a href="#vsto-add-ins">VSTO add-in guidance</a>.</span></span></td>
    </tr>
<tr>
        <td><span data-ttu-id="cc932-237">Enfant apparenté à la fenêtre Office</span><span class="sxs-lookup"><span data-stu-id="cc932-237">Child parented to Office window</span></span></td>
        <td><span data-ttu-id="cc932-238">Non</span><span class="sxs-lookup"><span data-stu-id="cc932-238">No</span></span></td>
        <td><span data-ttu-id="cc932-239">Voir <a href="#office-compatibility">Configurer Office pour optimiser la compatibilité</a>.</span><span class="sxs-lookup"><span data-stu-id="cc932-239">See <a href="#office-compatibility">Configure Office to optimize for compatibility</a>.</span></span></td>
</tr>
    <tr>
        <td rowspan="2"><span data-ttu-id="cc932-240"><a href="#custom-task-panes">Volet Office personnalisé</a></span><span class="sxs-lookup"><span data-stu-id="cc932-240"><a href="#custom-task-panes">Custom task pane</a></span></span></td>
        <td><span data-ttu-id="cc932-241">Niveau supérieur et descendants</span><span class="sxs-lookup"><span data-stu-id="cc932-241">Top and its descendants</span></span></td>
        <td><span data-ttu-id="cc932-242">Oui</span><span class="sxs-lookup"><span data-stu-id="cc932-242">Yes</span></span></td>
        <td><span data-ttu-id="cc932-243">Voir <a href="#top-level-window-management">Conseils fenêtre de niveau supérieur</a>.</span><span class="sxs-lookup"><span data-stu-id="cc932-243">See <a href="#top-level-window-management">top-level window guidance</a>.</span></span></td>
    </tr>
<tr>
        <td><span data-ttu-id="cc932-244">Enfant apparenté à la fenêtre Office</span><span class="sxs-lookup"><span data-stu-id="cc932-244">Child parented to Office window</span></span></td>
        <td><span data-ttu-id="cc932-245">Non</span><span class="sxs-lookup"><span data-stu-id="cc932-245">No</span></span></td>
        <td><span data-ttu-id="cc932-246">Voir <a href="#office-compatibility">Configurer Office pour optimiser la compatibilité</a>.</span><span class="sxs-lookup"><span data-stu-id="cc932-246">See <a href="#office-compatibility">Configure Office to optimize for compatibility</a>.</span></span></td>
</tr>
    <tr>
        <td rowspan="2"><span data-ttu-id="cc932-247"><a href="#com-add-ins">Complément COM</a></span><span class="sxs-lookup"><span data-stu-id="cc932-247"><a href="#com-add-ins">COM Add-in</a></span></span></td>
        <td><span data-ttu-id="cc932-248">Niveau supérieur et descendants</span><span class="sxs-lookup"><span data-stu-id="cc932-248">Top and its descendants</span></span></td>
        <td><span data-ttu-id="cc932-249">Oui</span><span class="sxs-lookup"><span data-stu-id="cc932-249">Yes</span></span></td>
        <td><span data-ttu-id="cc932-250">Voir <a href="#com-add-ins">Conseils complément COM</a>.</span><span class="sxs-lookup"><span data-stu-id="cc932-250">See <a href="#com-add-ins">COM Add-in guidance</a>.</span></span></td>
    </tr>
<tr>
        <td><span data-ttu-id="cc932-251">Enfant apparenté à la fenêtre Office</span><span class="sxs-lookup"><span data-stu-id="cc932-251">Child parented to Office window</span></span></td>
        <td><span data-ttu-id="cc932-252">Non</span><span class="sxs-lookup"><span data-stu-id="cc932-252">No</span></span></td>
        <td><span data-ttu-id="cc932-253">Voir <a href="#office-compatibility">Configurer Office pour optimiser la compatibilité</a>.</span><span class="sxs-lookup"><span data-stu-id="cc932-253">See <a href="#office-compatibility">Configure Office to optimize for compatibility</a>.</span></span></td>
</tr>
    <tr>
        <td rowspan="2"><span data-ttu-id="cc932-254"><a href="#activex-controls">Contrôle ActiveX</a></span><span class="sxs-lookup"><span data-stu-id="cc932-254"><a href="#activex-controls">ActiveX control</a></span></span></td>
        <td><span data-ttu-id="cc932-255">Niveau supérieur et descendants</span><span class="sxs-lookup"><span data-stu-id="cc932-255">Top and its descendants</span></span></td>
        <td><span data-ttu-id="cc932-256">Oui</span><span class="sxs-lookup"><span data-stu-id="cc932-256">Yes</span></span></td>
        <td><span data-ttu-id="cc932-257">Voir <a href="#activex-controls">Conseils contrôle ActiveX</a>.</span><span class="sxs-lookup"><span data-stu-id="cc932-257">See <a href="#activex-controls">ActiveX control guidance</a>.</span></span></td>
    </tr>
    <tr>
        <td><span data-ttu-id="cc932-258">Enfant apparenté à la fenêtre Office</span><span class="sxs-lookup"><span data-stu-id="cc932-258">Child parented to Office window</span></span></td>
        <td><span data-ttu-id="cc932-259">Oui</span><span class="sxs-lookup"><span data-stu-id="cc932-259">Yes</span></span></td>
    </tr>
    <tr>
        <td><span data-ttu-id="cc932-260"><a href="#web-add-ins">Complément Web</a></span><span class="sxs-lookup"><span data-stu-id="cc932-260"><a href="#web-add-ins">Web Add-in</a></span></span></td>
        <td><span data-ttu-id="cc932-261">N/A</span><span class="sxs-lookup"><span data-stu-id="cc932-261">NA</span></span></td>
        <td><span data-ttu-id="cc932-262">Oui</span><span class="sxs-lookup"><span data-stu-id="cc932-262">Yes</span></span></td>
        <td><span data-ttu-id="cc932-263">Voir <a href="#web-add-ins">Conseils complément Office web</a>.</span><span class="sxs-lookup"><span data-stu-id="cc932-263">See <a href="#web-add-ins">Office web add-in guidance</a>.</span></span></td>
    </tr>
    <tr>
        <td><span data-ttu-id="cc932-264"><a href="#ribbon-extensibility">Extension du ruban</a></span><span class="sxs-lookup"><span data-stu-id="cc932-264"><a href="#ribbon-extensibility">Ribbon extension</a></span></span></td>
        <td><span data-ttu-id="cc932-265">N/A</span><span class="sxs-lookup"><span data-stu-id="cc932-265">NA</span></span></td>
        <td><span data-ttu-id="cc932-266">N/A</span><span class="sxs-lookup"><span data-stu-id="cc932-266">NA</span></span></td>
        <td><span data-ttu-id="cc932-267">Voir <a href="#ribbon-extensibility">Conseils extension ruban</a>.</span><span class="sxs-lookup"><span data-stu-id="cc932-267">See <a href="#ribbon-extensibility">Ribbon extension guidance</a>.</span></span></td>
    </tr>
    <tr>
        <td><span data-ttu-id="cc932-268"><a href="#ole">Client ou serveur OLE</a></span><span class="sxs-lookup"><span data-stu-id="cc932-268"><a href="#ole">OLE server or client</a></span></span></td>
        <td><span data-ttu-id="cc932-269">N/A</span><span class="sxs-lookup"><span data-stu-id="cc932-269">NA</span></span></td>
        <td><span data-ttu-id="cc932-270">N/A</span><span class="sxs-lookup"><span data-stu-id="cc932-270">NA</span></span></td>
        <td><span data-ttu-id="cc932-271">Voir <a href="#ole">Conseils client/serveur OLE</a>.</span><span class="sxs-lookup"><span data-stu-id="cc932-271">See <a href="#ole">OLE server/client guidance</a>.</span></span></td>
    </tr>
</tbody>
</table>

<h3 id="vsto-add-ins"><span data-ttu-id="cc932-272">Complément VSTO</span><span class="sxs-lookup"><span data-stu-id="cc932-272">VSTO add-in</span></span></h3>

<span data-ttu-id="cc932-273">Si votre complément VSTO crée des fenêtres enfant apparentées à n’importe quelle fenêtre Office, assurez-vous qu’elles correspondent à la résolution de présence de leur fenêtre parent.</span><span class="sxs-lookup"><span data-stu-id="cc932-273">If your VSTO add-in creates child windows that are parented to any Office windows, be sure they match the DPI awareness of their parent window.</span></span> <span data-ttu-id="cc932-274">Vous pouvez utiliser la fonction[GetWindowdpiAwarenessContext](https://docs.microsoft.com/en-us/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext) pour obtenir la résolution de présence de la fenêtre parent.</span><span class="sxs-lookup"><span data-stu-id="cc932-274">You can use the [GetWindowdpiAwarenessContext](https://docs.microsoft.com/en-us/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext) function to get the DPI awareness of the parent window.</span></span> <span data-ttu-id="cc932-275">Vos fenêtres enfants ne recevront pas les notifications de modification PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-275">Your child windows will not get any DPI change notifications.</span></span> <span data-ttu-id="cc932-276">Si votre solution n’est pas affichée correctement, les utilisateurs doivent configurer Office en mode de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="cc932-276">If your solution is not rendering correctly, users will need to put Office into compatibility mode.</span></span>

<span data-ttu-id="cc932-277">Pour n’importe quelle fenêtre de niveau supérieur que votre complément VSTO crée, vous pouvez les définir sur n’importe quel mode de présence PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-277">For any top-level windows your VSTO add-in creates, you can set them to any DPI awareness mode.</span></span> <span data-ttu-id="cc932-278">L’exemple de code suivant explique comment configurer la présence de PPP souhaitée et comment répondre aux modifications PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-278">The following sample code shows how to set up the desired DPI awareness, and how to respond to DPI changes.</span></span> <span data-ttu-id="cc932-279">Vous devrez également ajuster votre app.config, comme décrit dans l’article [Prise en charge de la haute résolution dans Windows Forms](https://docs.microsoft.com/en-us/dotnet/framework/winforms/high-dpi-support-in-windows-forms).</span><span class="sxs-lookup"><span data-stu-id="cc932-279">You will also need to adjust your app.config, as described in the [High DPI support in Windows Forms](https://docs.microsoft.com/en-us/dotnet/framework/winforms/high-dpi-support-in-windows-forms) article.</span></span> 

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

<h3 id="custom-task-panes"><span data-ttu-id="cc932-280">Volets des tâches personnalisés</span><span class="sxs-lookup"><span data-stu-id="cc932-280">Custom task panes</span></span></h3>

<span data-ttu-id="cc932-281">Un volet de tâches personnalisé est créé comme fenêtre enfant par Office.</span><span class="sxs-lookup"><span data-stu-id="cc932-281">A custom task pane is created as a child window by Office.</span></span> <span data-ttu-id="cc932-282">Lors de l’exécution sur Windows Fall Creators Update (1709), votre volet Office personnalisé s’exécute en utilisant le même mode de présence PPP qu’Office.</span><span class="sxs-lookup"><span data-stu-id="cc932-282">When running on Windows Fall Creators Update (1709), your custom task pane will run using the same DPI awareness mode as Office.</span></span> <span data-ttu-id="cc932-283">Lors de l’exécution sur la mise à jour avril 2018 Windows (1803) et versions ultérieures, votre volet de tâches personnalisé s’exécutera sur le mode de présence système PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-283">When running on Windows April 2018 Update (1803) and later, your custom task pane will run using System DPI awareness mode.</span></span> 

<span data-ttu-id="cc932-284">Comme les volets de tâches personnalisés sont des fenêtres enfants, ils ne peuvent pas recevoir de notifications PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-284">Because custom task panes are child windows, they cannot receive DPI notifications.</span></span> <span data-ttu-id="cc932-285">S’ils sont affichés incorrectement, l’utilisateur devra utiliser le[mode de compatibilité Office PPP](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span><span class="sxs-lookup"><span data-stu-id="cc932-285">If they are drawing incorrectly, the user will need to use [Office DPI compatibility mode](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span></span>
<span data-ttu-id="cc932-286">Si votre volet de tâches personnalisé crée des fenêtres de niveau supérieur, ces fenêtres peuvent s’exécuter dans n’importe quel mode de présence PPP et recevoir des notifications de modification PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-286">If your custom task pane creates top-level windows, those windows can run in any DPI awareness mode and receive DPI change notifications.</span></span> <span data-ttu-id="cc932-287">Pour plus d’informations, voir la section [Gestion de la fenêtre de niveau supérieur](#Top-level-window-management) de cet article.</span><span class="sxs-lookup"><span data-stu-id="cc932-287">For more information, see the [Top-level window management](#Top-level-window-management) section in this article.</span></span>

<h3 id="com-add-ins"><span data-ttu-id="cc932-288">Compléments COM</span><span class="sxs-lookup"><span data-stu-id="cc932-288">COM add-ins</span></span></h3>

<span data-ttu-id="cc932-289">Les compléments COM qui créent des fenêtres de niveau supérieur peuvent recevoir des notifications PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-289">COM add-ins that create top-level windows can receive DPI notifications.</span></span> <span data-ttu-id="cc932-290">Vous devez créer un [bloc de contexte](#Build-a-context-block-for-incoming-thread-calls) pour définir le thread à la présence PPP souhaitée pour la fenêtre, puis créer la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cc932-290">You should create a [context block](#Build-a-context-block-for-incoming-thread-calls) to set the thread to the DPI awareness that you want for your window, then create your window.</span></span> <span data-ttu-id="cc932-291">Il y a beaucoup à gagner à gérer les notifications PPP correctement, veillez donc à lire [Développement d’applications bureau à haute résolution sur Windows](https://docs.microsoft.com/en-us/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="cc932-291">There’s a lot to handling the DPI notifications correctly, so be sure to read [High DPI Desktop Application Development on Windows](https://docs.microsoft.com/en-us/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics) for more details.</span></span>

<span data-ttu-id="cc932-292">Le message [WM_DPICHANGED](https://msdn.microsoft.com/en-us/library/windows/desktop/dn312083(v=vs.85).aspx) est envoyé lorsque le PPP pour une fenêtre a changé.</span><span class="sxs-lookup"><span data-stu-id="cc932-292">The [WM_DPICHANGED](https://msdn.microsoft.com/en-us/library/windows/desktop/dn312083(v=vs.85).aspx) message is sent when the DPI for a window has changed.</span></span>  <span data-ttu-id="cc932-293">Dans le code non géré, ce message est géré par la [Procédure de fenêtre](https://msdn.microsoft.com/en-us/library/windows/desktop/ms633570(v=vs.85).aspx) pour le HWND.</span><span class="sxs-lookup"><span data-stu-id="cc932-293">In unmanaged code, this message is handled by the [Window Procedure](https://msdn.microsoft.com/en-us/library/windows/desktop/ms633570(v=vs.85).aspx) for the HWND.</span></span>  <span data-ttu-id="cc932-294">Un exemple de code de modification du gestionnaire PPP est accessible dans l’article [WM_DPICHANGED](https://msdn.microsoft.com/en-us/library/windows/desktop/dn312083(v=vs.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="cc932-294">Sample DPI change handler code can be found in the [WM_DPICHANGED](https://msdn.microsoft.com/en-us/library/windows/desktop/dn312083(v=vs.85).aspx) article.</span></span> 

<span data-ttu-id="cc932-295">Les compléments COM qui montrent les fenêtres enfants apparentées à une fenêtre dans Office ne peuvent pas recevoir de notifications PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-295">COM add-ins that show child windows that are parented to a window in Office cannot receive DPI notifications.</span></span> <span data-ttu-id="cc932-296">S’ils sont affichés incorrectement, l’utilisateur devra utiliser le[mode de compatibilité Office PPP](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span><span class="sxs-lookup"><span data-stu-id="cc932-296">If they are drawing incorrectly, the user will need to use [Office DPI compatibility mode](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span></span>

<h3 id="activex-controls"><span data-ttu-id="cc932-297">Contrôles ActiveX</span><span class="sxs-lookup"><span data-stu-id="cc932-297">ActiveX controls</span></span></h3>

<span data-ttu-id="cc932-298">Comment prendre en charge la mise à l’échelle PPP dans les contrôles ActiveX dépend de si le contrôle dans une fenêtre ou sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cc932-298">How to support DPI scaling in ActiveX controls depends on whether the control is windowed or windowless.</span></span>

#### <a name="windowed-activex-controls"></a><span data-ttu-id="cc932-299">Contrôles ActiveX dans une fenêtre</span><span class="sxs-lookup"><span data-stu-id="cc932-299">Windowed ActiveX controls</span></span>

<span data-ttu-id="cc932-300">Les contrôles ActiveX dans une fenêtre reçoivent un message WM_SIZE chaque fois que le contrôle est redimensionné.</span><span class="sxs-lookup"><span data-stu-id="cc932-300">Windowed ActiveX controls receive a WM_SIZE message each time the control is resized.</span></span>  <span data-ttu-id="cc932-301">Lorsque cet événement est déclenché, le code gestionnaire d’événements peut d’appeler la fonction [GetDpiForWindow](https://docs.microsoft.com/en-us/windows/desktop/api/winuser/nf-winuser-getdpiforwindow) utilisant HWND du contrôle pour obtenir le PPP, calculer les différences de facteur échelle et ajuster en conséquence.</span><span class="sxs-lookup"><span data-stu-id="cc932-301">When this event is triggered, the event handler code can call the [GetDpiForWindow](https://docs.microsoft.com/en-us/windows/desktop/api/winuser/nf-winuser-getdpiforwindow) function using the HWND of the control to get the DPI, calculate the scale factor differences, and adjust as needed.</span></span> 

<span data-ttu-id="cc932-302">L’exemple suivant permet au contrôle ActiveX basé sur MFC de répondre à l’événement **OnSize**.</span><span class="sxs-lookup"><span data-stu-id="cc932-302">The following example enables an MFC-based ActiveX control to respond to the **OnSize** event.</span></span> 

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

#### <a name="windowless-activex-controls"></a><span data-ttu-id="cc932-303">Contrôles ActiveX sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="cc932-303">Windowless ActiveX controls</span></span>

<span data-ttu-id="cc932-304">Les contrôles ActiveX ne sont pas garantis d’avoir un HWND.</span><span class="sxs-lookup"><span data-stu-id="cc932-304">Windowless ActiveX controls are not guaranteed have an HWND.</span></span>  <span data-ttu-id="cc932-305">Quand un contrôle ActiveX est inséré sur une zone de document, il placé en mode Création.</span><span class="sxs-lookup"><span data-stu-id="cc932-305">When an ActiveX control is inserted onto a document canvas, it is put into design mode.</span></span>  <span data-ttu-id="cc932-306">Dans les applications Office, le conteneur d’hébergement renvoie 0 pour l’appel à hDC -> GetWindow() dans le :: OnDraw événement lorsque le contrôle est en mode Création.</span><span class="sxs-lookup"><span data-stu-id="cc932-306">In Office applications, the hosting container will return 0 for the call to hDC->GetWindow() in the ::OnDraw event when the control is in design mode.</span></span>  <span data-ttu-id="cc932-307">Un PPP fiable ne peut pas être récupéré dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="cc932-307">A reliable DPI cannot be retrieved in this case.</span></span> 

<span data-ttu-id="cc932-308">Toutefois, lorsque le contrôle est en mode d’exécution, Office renverra HWND où le contrôle doit être affiché.</span><span class="sxs-lookup"><span data-stu-id="cc932-308">However, when the control is in runtime mode, Office will return the HWND where the control is to be drawn.</span></span>  <span data-ttu-id="cc932-309">Dans ce cas, le développeur de contrôle peut appeler [GetDpiForWindow](https://docs.microsoft.com/en-us/windows/desktop/api/winuser/nf-winuser-getdpiforwindow) afin de recevoir les polices, l’échelle, contrôles PPP actuels et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="cc932-309">In this case, the control developer can call [GetDpiForWindow](https://docs.microsoft.com/en-us/windows/desktop/api/winuser/nf-winuser-getdpiforwindow) and get the current DPI and scale fonts, controls, and so on.</span></span> 

<h3 id="ribbon-extensibility"><span data-ttu-id="cc932-310">Extensibilité du ruban </span><span class="sxs-lookup"><span data-stu-id="cc932-310">Custom ribbon extensibility</span></span></h3>

<span data-ttu-id="cc932-311">Les rappels Office pour les contrôles de ruban personnalisés sont également une présence thread PPP de système PPP pris en compte.</span><span class="sxs-lookup"><span data-stu-id="cc932-311">Any callbacks from Office for custom ribbon controls will be in a DPI thread awareness of System DPI aware.</span></span>  <span data-ttu-id="cc932-312">Si votre solution attend une présence de thread PPP différente, vous devez implémenter un bloc de contexte pour configurer la présence de thread attendue.</span><span class="sxs-lookup"><span data-stu-id="cc932-312">If your solution is expecting a different DPI thread awareness, you should implement a context block to set the thread awareness as expected.</span></span> <span data-ttu-id="cc932-313">Pour plus d’informations, voir [Créer un bloc de contexte](#Build-a-context-block-for-incoming-thread-calls).</span><span class="sxs-lookup"><span data-stu-id="cc932-313">For more information, see [Build a context block](#Build-a-context-block-for-incoming-thread-calls).</span></span>

<h3 id="ole"><span data-ttu-id="cc932-314">Serveurs et clients OLE</span><span class="sxs-lookup"><span data-stu-id="cc932-314">OLE clients and servers</span></span></h3>

<span data-ttu-id="cc932-315">Lorsqu’un serveur OLE est hébergé dans un conteneur de client OLE, vous ne pouvez pas fournir d’informations PPP actuelles ni prises en charge.</span><span class="sxs-lookup"><span data-stu-id="cc932-315">When an OLE server is hosted within an OLE client container, you currently can’t provide current or supported DPI information.</span></span> <span data-ttu-id="cc932-316">Cela peut provoquer des problèmes, car certaines combinaisons de modes mixtes de fenêtre parent à fenêtre enfant ne sont pas pris en charge par l’architecture actuelle de Windows.</span><span class="sxs-lookup"><span data-stu-id="cc932-316">This can cause problems because some combinations of parent to child window mixed modes are not supported by the current Windows architecture.</span></span> <span data-ttu-id="cc932-317">Si Word ou Excel détecte qu’il existe plusieurs moniteurs avec différentes échelles PPP, ils ne prennent pas en charge l’activation sur place.</span><span class="sxs-lookup"><span data-stu-id="cc932-317">If Word or Excel detect that there are multiple monitors with different DPI scales, they will not support in-place activation.</span></span> <span data-ttu-id="cc932-318">Votre serveur OLE s’activera en externe.</span><span class="sxs-lookup"><span data-stu-id="cc932-318">Your OLE server will activate out-of-place.</span></span> <span data-ttu-id="cc932-319">Si vous rencontrez des problèmes avec les interactions de serveur OLE, l’utilisateur devra utiliser le [mode de compatibilité Office PPP](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span><span class="sxs-lookup"><span data-stu-id="cc932-319">If you are experiencing issues with OLE server interactions, the user will need to use [Office DPI compatibility mode](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span></span>

<h3 id="web-add-ins"><span data-ttu-id="cc932-320">Compléments Office web</span><span class="sxs-lookup"><span data-stu-id="cc932-320">Office Web Add-ins</span></span></h3>

<span data-ttu-id="cc932-321">Les compléments Office créés à l’aide de l’API JavaScript Office s’exécutent à l’intérieur d’un contrôle de navigateur.</span><span class="sxs-lookup"><span data-stu-id="cc932-321">Office Add-ins built using the Office JavaScript API run inside a browser control.</span></span> <span data-ttu-id="cc932-322">Vous pouvez gérer la mise à l’échelle PPP à l’aide des mêmes techniques utilisées dans n’importe quelle conception d’applications web.</span><span class="sxs-lookup"><span data-stu-id="cc932-322">You can handle DPI scaling using the same techniques used in any web app design.</span></span> <span data-ttu-id="cc932-323">Plusieurs ressources en ligne sont disponibles pour vous aider à créer une page web pour les écrans haute résolution.</span><span class="sxs-lookup"><span data-stu-id="cc932-323">Many online resources are available to help design a web page for high resolution screens.</span></span>

## <a name="verify-that-your-solution-supports-dpi-scaling"></a><span data-ttu-id="cc932-324">Vérifier que votre solution prend en charge la mise à l’échelle PPP</span><span class="sxs-lookup"><span data-stu-id="cc932-324">Verify that your solution supports DPI scaling</span></span>

<span data-ttu-id="cc932-325">Une fois que vous avez mis à jour votre application pour prendre en charge la mise à l’échelle PPP, vous devez valider vos modifications dans un environnement mixte PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-325">After you have updated your application to support DPI scaling, you should validate your changes in a mixed-DPI environment.</span></span> <span data-ttu-id="cc932-326">Vérifiez que votre code d’interface utilisateur répond correctement aux modifications PPP quand les fenêtres de votre solution sont déplacées d’un affichage à un autre ayant des valeurs PPP différentes.</span><span class="sxs-lookup"><span data-stu-id="cc932-326">Validate that your UI code responds properly to DPI changes when your solution’s windows are moved from one display to another that has different DPI values.</span></span> <span data-ttu-id="cc932-327">Pour plus d’informations sur les techniques de test de redimensionnement PPP, voir [Développement d’applications bureau haute résolution sur Windows](https://docs.microsoft.com/en-us/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics).</span><span class="sxs-lookup"><span data-stu-id="cc932-327">For more information about DPI scaling testing techniques, see [High DPI Desktop Application Development on Windows](https://docs.microsoft.com/en-us/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics).</span></span>

<span data-ttu-id="cc932-328">Vous pouvez également trouver ces techniques supplémentaires utiles :</span><span class="sxs-lookup"><span data-stu-id="cc932-328">You might also find these additional techniques helpful:</span></span>

- <span data-ttu-id="cc932-329">Avec un ordinateur portable, vous pouvez configurer le moniteur principal à un moniteur externe, puis détacher l’ordinateur portable.</span><span class="sxs-lookup"><span data-stu-id="cc932-329">With a laptop, you can set the primary monitor to an external monitor, then undock the laptop.</span></span> <span data-ttu-id="cc932-330">Cela force le moniteur principal à aligner son affichage à celui de l’ordinateur portable.</span><span class="sxs-lookup"><span data-stu-id="cc932-330">This will force the primary monitor to change to the laptop display.</span></span>
- <span data-ttu-id="cc932-331">Utiliser l’open source [WinSpy ++ outil](https://github.com/BissetJ/winspy/releases) afin de déboguer.</span><span class="sxs-lookup"><span data-stu-id="cc932-331">Use the open source [WinSpy++ tool](https://github.com/BissetJ/winspy/releases) to help debug.</span></span> <span data-ttu-id="cc932-332">Vous pouvez l’utiliser pour afficher le paramètre de présence PPP de n’importe quelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cc932-332">You can use it to see the DPI awareness setting of any window.</span></span>
- <span data-ttu-id="cc932-333">Vous pouvez utiliser le bureau à distance pour tester plusieurs moniteurs sur un ordinateur distant en sélectionnant Utiliser tous mes moniteurs pour la session distante sous l’onglet Affichage, comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="cc932-333">You can use remote desktop to test multiple monitors on a remote computer by selecting Use all my monitors for the remote session on the Display tab, as shown in the following screenshot.</span></span>

![L’application de Connexion Bureau à distance montrant l’onglet Affichage, et sélectionnant Utiliser mes moniteurs pour la session distante.](./media/remote-desktop-use-all-monitors.png)

## <a name="see-also"></a><span data-ttu-id="cc932-335">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc932-335">See also</span></span>

### <a name="articles"></a><span data-ttu-id="cc932-336">Articles</span><span class="sxs-lookup"><span data-stu-id="cc932-336">Articles</span></span>

- <span data-ttu-id="cc932-337">
  [Écrire un bureau PPP pris en compte et Applications Win32](https://msdn.microsoft.com/en-us/library/windows/desktop/dn469266(v=vs.85).aspx) fournit une vue d’ensemble et un guide pour écrire des applications de bureau Win32.</span><span class="sxs-lookup"><span data-stu-id="cc932-337">[Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/en-us/library/windows/desktop/dn469266(v=vs.85).aspx) provides a general overview and guide for writing Win32 desktop applications.</span></span> <span data-ttu-id="cc932-338">Bon nombre des techniques décrites dans cet article peuvent être appliquées aux solutions d’extensibilité Office.</span><span class="sxs-lookup"><span data-stu-id="cc932-338">Many of the same techniques described in this article will apply to Office extensibility solutions.</span></span>
- <span data-ttu-id="cc932-339">
  [Mise à l’échelle PPP mode mixte et API PPP pris en compte](https://msdn.microsoft.com/en-us/library/windows/desktop/mt744321(v=vs.85).aspx) a une liste d’API connexes à PPP.</span><span class="sxs-lookup"><span data-stu-id="cc932-339">[Mixed-Mode DPI Scaling and DPI-aware APIs](https://msdn.microsoft.com/en-us/library/windows/desktop/mt744321(v=vs.85).aspx) has a list of APIs related to DPI.</span></span>
- <span data-ttu-id="cc932-340">[Guie de développeur - Par moniteur PPP - Aperçu WPF](https://github.com/Microsoft/WPF-Samples/blob/master/PerMonitorDPI/Developer%20Guide%20-%20Per%20Monitor%20DPI%20-%20WPF%20Preview.docx) couvre le guide de développement d’application WPF pour créer des applications WPF PPP pris en compte.</span><span class="sxs-lookup"><span data-stu-id="cc932-340">[Developer Guide - Per Monitor DPI - WPF Preview](https://github.com/Microsoft/WPF-Samples/blob/master/PerMonitorDPI/Developer%20Guide%20-%20Per%20Monitor%20DPI%20-%20WPF%20Preview.docx) covers the WPF app development guide for building DPI-aware WPF apps.</span></span>
- <span data-ttu-id="cc932-341">[Support technique Office pour l’affichage haute définition](https://support.office.com/en-us/article/Office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d) fournit des informations sur la manière dont un utilisateur peut définir Office afin d’optimiser pour assurer la compatibilité si votre solution Office n’est pas prise en charge correctement lorsque le PPP change.</span><span class="sxs-lookup"><span data-stu-id="cc932-341">[Office support for high definition displays](https://support.office.com/en-us/article/Office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d) provides information about how a user can set Office to optimize for compatibility if your Office solution is not supported properly when the DPI changes.</span></span>
- <span data-ttu-id="cc932-342">[Afficher les modifications de mise à l’échelle pour la Mise à jour anniversaire Windows 10](https://blogs.technet.microsoft.com/askcore/2016/08/16/display-scaling-changes-for-the-windows-10-anniversary-update/) est un billet de blog qui présente les modifications introduites avec la mise à jour anniversaire Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cc932-342">[Display Scaling changes for the Windows 10 Anniversary Update](https://blogs.technet.microsoft.com/askcore/2016/08/16/display-scaling-changes-for-the-windows-10-anniversary-update/) is a blog post that covers changes introduce with the Windows 10 Anniversary update.</span></span> 
- <span data-ttu-id="cc932-343">[Gérer DPI_AWARENESS_CONTEXT](https://docs.microsoft.com/en-us/windows/desktop/hidpi/dpi-awareness-context) contient les détails de programme sur les valeurs et définitions de DPI_AWARENESS_CONTEXT.</span><span class="sxs-lookup"><span data-stu-id="cc932-343">[DPI_AWARENESS_CONTEXT handle](https://docs.microsoft.com/en-us/windows/desktop/hidpi/dpi-awareness-context) has programming details on the DPI_AWARENESS_CONTEXT values and definitions.</span></span>
- <span data-ttu-id="cc932-344">[Développement d’applications bureau PPP élevée sur Windows](https://docs.microsoft.com/en-us/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#testing-your-changes) inclut des informations sur le test dans la section Testez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="cc932-344">[High DPI Desktop Application Development on Windows](https://docs.microsoft.com/en-us/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#testing-your-changes) includes information about testing in the Testing Your Changes section.</span></span>

### <a name="code-samples"></a><span data-ttu-id="cc932-345">Exemples de code</span><span class="sxs-lookup"><span data-stu-id="cc932-345">Code samples</span></span>

- [<span data-ttu-id="cc932-346">Exemple de présence PPP par fenêtre</span><span class="sxs-lookup"><span data-stu-id="cc932-346">Per-window DPI Awareness sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow)
- [<span data-ttu-id="cc932-347">Exemples de PPP dynamiques</span><span class="sxs-lookup"><span data-stu-id="cc932-347">Dynamic DPI sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DynamicDPI)
- [<span data-ttu-id="cc932-348">Exemple WPF par moniteur pris en compte</span><span class="sxs-lookup"><span data-stu-id="cc932-348">Per-Monitor Aware WPF sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)
