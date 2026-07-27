# ==========================================
# Project: NextForge
# Description:
# A forward-leading repository focused on innovation,
# modern practices, and strong code foundations.
# ==========================================


# ---------- main.py ----------
"""
Main entry point for NextForge.
"""

from core.innovation import 
from core.foundation import FoundationCore
from core.modern import ModernPractices


def run():
    print("🚀 NextForge Initialized")
    print("💡 Innovation | ⚡ Modern Practices | 🧱 Strong Foundations\n")

    innovation = InnovationLab()
    foundation = FoundationCore()
    modern = ModernPractices()

    ideas = ["automation", "cloud", "analytics"]

    print("💡 Innovation Pipeline:", innovation.expand(ideas))
    print("🧱 Foundation Score:", foundation.strength_score([10, 12, 11, 13]))
    print("⚡ Modern Workflow:", modern.transform([1, 2, 3, 4]))


if __name__ == "__main__":
    run()


# ---------- core/innovation.py ----------
"""
Innovation-focused experimentation module.
"""

class InnovationLab:
    """Explores and expands new ideas."""

    def expand(self, ideas):
        """Convert raw ideas into innovation candidates."""
        return [f"next_{idea}" for idea in ideas]

    def prototype(self, func, data):
        """Quickly test a prototype implementation."""
        return [func(x) for x in data]


# ---------- core/foundation.py ----------
"""
Core foundation utilities for reliability and structure.
"""

import statistics

class FoundationCore:
    """Measures and maintains strong software foundations."""

    def strength_score(self, metrics):
        """Calculate a foundation strength score."""
        if not metrics:
            return 0.0

        mean = statistics.mean(metrics)
        variance = statistics.pvariance(metrics)

        return round(mean / (1 + variance), 3)

    def validate(self, values):
        """Validate that all values are numeric."""
        return all(isinstance(v, (int, float)) for v in values)


# ---------- core/modern.py ----------
"""
Modern development practices and utilities.
"""

class ModernPractices:
    """Applies modern transformation and workflow patterns."""

    def transform(self, values):
        """Functional-style data transformation."""
        return list(map(lambda x: x * 2, values))

    def filter_active(self, values, threshold):
        """Filter values above a threshold."""
        return [v for v in values if v > threshold]


# ---------- tests/test_innovation.py ----------
from core.innovation import InnovationLab

def test_expand():
    lab = InnovationLab()
    assert "next_ai" in lab.expand(["ai"])


# ---------- tests/test_foundation.py ----------
from core.foundation import FoundationCore

def test_strength_score():
    core = FoundationCore()
    assert core.strength_score([10, 11, 12]) > 0


# ---------- tests/test_modern.py ----------
from core.modern import ModernPractices

def test_transform():
    modern = ModernPractices()
    assert modern.transform([1, 2]) == [2, 4]
